pipeline {
 agent none
  stages {
    stage ('Analysis ShiftLeft'){
     agent any
      steps{
        sh 'mvn clean package'
        sh '/usr/local/bin/sl analyze --app HelloShiftLeft --java target/hello-shiftleft-0.0.1.jar'
      }
    }
    
  }
  
}
