pipeline {
  agent { label 'UbuntuSlave01' }
libraries {
 lib('lib-demo@stage') 
} 
  stages {
    stage('Git Checkout') {
        steps {
            git branch: 'dev',
            credentialsId: '8b5c313a-4c4a-411c-b276-6e5b386558fe',
            url: 'https://github.com/devopssoftermii/nodejs-hello-world.git'
            sh "ls -lat"
          }
    }
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
