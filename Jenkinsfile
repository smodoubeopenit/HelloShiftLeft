pipeline {
  agent {
    docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
     }
    stages {
      stage('Build') {
            
            steps {
                sh 'mvn clean package' 
                archiveArtifacts artifacts: '**/target/hello-shiftleft-0.0.1.jar', fingerprint: true 
            }
        }
      stage('SLAnalyze') {
       
          steps{
            sh '/usr/local/bin/sl analyze --app HelloShiftLeft --java target/hello-shiftleft-0.0.1.jar'
            }
        }
    }
}
