pipeline {
  agent none
    tools {
        maven 'Maven 3.3.9'
        jdk 'jdk8'
    }
    stages {
      stage('Build') {
            agent any
            steps {
                sh 'mvn clean package' 
                archiveArtifacts artifacts: '**/target/hello-shiftleft-0.0.1.jar', fingerprint: true 
            }
        }
      stage('SLAnalyze') {
          agent any
          steps{
            sh '/usr/local/bin/sl analyze --app HelloShiftLeft --java target/hello-shiftleft-0.0.1.jar'
            }
        }
    }
}
