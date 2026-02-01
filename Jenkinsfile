pipeline
{
    agent any

    stages
    {
        stage('Checkout')
        {
            steps
            {
                echo "Checking out source code"
            }
        }

        stage('Main Branch Build')
        {
            when
            {
                branch 'main'
            }
            steps
            {
                echo "Production build for MAIN branch"
            }
        }

        stage('Feature Branch Build')
        {
            when
            {
                branch 'feature-*'
            }
            steps
            {
                echo "Testing build for FEATURE branch"
            }
        }

        stage('Release Branch Build')
        {
            when
            {
                branch 'release-*'
            }
            steps
            {
                echo "Staging build for RELEASE branch"
            }
        }
    }
}
