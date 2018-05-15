pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }

    stage('Unit test') {
          steps {
            // Compile and run the unit tests for the app and its dependencies
            sh './gradlew testDebugUnitTest testDebugUnitTest'

            // Analyse the test results and update the build result as appropriate
            junit '**/TEST-*.xml'
          }
        }

    }
}