pipeline {
    agent any

    stages {

        stage('Main Branch Build') {
            when {
                branch 'main'
            }
            steps {
                echo 'Running build for MAIN branch'
                echo 'This represents full build'
            }
        }

        stage('Feature Branch Build') {
            when {
                expression { env.BRANCH_NAME.startsWith('feature/') }
            }
            steps {
                echo 'Running tests only for FEATURE branch'
            }
        }

        stage('Release Branch Build') {
            when {
                expression { env.BRANCH_NAME.startsWith('release/') }
            }
            steps {
                echo 'Running build and deploy for RELEASE branch'
            }
        }
    }
}
