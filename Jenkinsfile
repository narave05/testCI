pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
       stage('Unit test') {
             steps {
               // Compile and run the unit tests for the app and its dependencies
               sh './gradlew testDebugUnitTest'

               // Analyse the test results and update the build result as appropriate
               junit '**/TEST-*.xml'
             }
           }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}