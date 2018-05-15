pipeline {
    agent {
        // Run on a build agent where we have the Android SDK installed
        label 'android'
      }


    stages {


    stage('Compile') {
         steps {
           // Compile the app and its dependencies
           sh './gradlew compileDebugSources'
         }
       }
       stage('Run unit test') {
         steps {
           // Compile and run the unit tests for the app and its dependencies
           sh './gradlew assembleAndroidTest'

           // Analyse the test results and update the build result as appropriate
           //junit '**/TEST-*.xml'
         }
       }
       stage('Build APK') {
         steps {
           // Finish building and packaging the APK
           sh './gradlew assembleDebug'

           // Archive the APKs so that they can be downloaded from Jenkins
           archiveArtifacts '**/*.apk'
         }
       }

    }
}