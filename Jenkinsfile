pipeline {
  agent { label 'UbuntuSlave01' }
libraries {
 lib('lib-demo@stage') 
} 
  stages {
    stage ('build image') {
        sh "docker build . -t hellonode:1"
    }
    stage ('demo') {
      agent {
        docker { image 'hellonode' }
      }
      steps {
        sh "node --version"
        }
    }    
  }
}
