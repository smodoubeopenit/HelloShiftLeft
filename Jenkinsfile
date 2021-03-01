pipeline {
  agent none
    stages {
      stage('SLAnalyze') {
        agent any
          steps {
          dir("/home/modou/Desktop/cno/cno-api/") {
          sh '/usr/local/bin/sl analyze --app CnoApi'
          }
        }
     }
    }
}
