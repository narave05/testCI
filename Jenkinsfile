pipeline {
   agent any

   stages {
       stage('Unit test') {
            steps {
            echo 'Hello World'
              // Compile and run the unit tests for the app and its dependencies

               sh 'chmod +x gradlew'
               sh './gradlew testDebugUnitTest'
            }
          }
   }
}