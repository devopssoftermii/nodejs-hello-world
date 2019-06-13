pipeline {
  agent { label 'UbuntuSlave01' }
libraries {
 lib('lib-demo@master') 
} 
  stages {
    stage ('demo') {
      agent {
        docker { image 'node:7-alpine' }
      }
      steps {
        sh "node --version"
        }
    }    
  }
}
