pipeline {
  agent none
    stages {
      stage('SLAnalyze') {
        agent any
          steps{
            sh '/usr/local/bin/sl analyze --app HelloShiftLeft --java target/hello-shiftleft-0.0.1.jar'
          }
        }
    }
}
