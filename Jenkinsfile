pipeline {
   agent any

   stages {

   stage('Compile') {
             steps {
               // Compile the app and its dependencies
               sh './gradlew compileDebugSources'
             }
           }

       stage('Unit test') {
            steps {
            echo 'Hello World'
              // Compile and run the unit tests for the app and its dependencies

               sh './gradlew testDebugUnitTest testDebugUnitTest'
            }
          }
   }
}