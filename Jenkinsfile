pipeline {
  agent { label 'UbuntuSlave01' }
libraries {
 lib('lib-demo@master') 
} 
  stages {
    stage ('demo') {
      steps {
        hello 'somebody'
        }
    }    
  }
}
