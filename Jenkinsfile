pipeline {
    
   environment {
    registry = "kleku81/test_node"
    registryCredential = 'Docker_HUB'
  }
    agent { dockerfile true }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'svn --version'
            }
        stage('Building image') {
            steps{
                script {
                      docker.build registry + ":$BUILD_NUMBER"
        }
      }
    }
        }
    }
   
    
  
}
