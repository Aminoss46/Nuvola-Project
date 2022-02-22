pipeline {
  environment {
    registry = 'akkafranck/nuvola'
    registryCredential = 'DockerHub'
  }
    agent any
    stages {
        stage('Build_Docker_Image') {
            steps {
                sh 'docker build -t nuvola:2.0 .'
            }
        }
        stage('Deploy Image') {
	  steps{
            script {
              docker.withRegistry('',registryCredential){
                dockerImage.push()
              }
            }
          }        
        }
    }
}
