pipeline {
  environment {
    registry = ''
    registryCredential = 'DockerHub'
    imagename = 'akkafranck/nuvola'
  }
    agent any
    stages {
        stage('Build_Docker_Image') {
            steps {
                //sh 'docker build -t nuvola:2.0 .'
              script {
                registry = docker.build imagename
              }
            }
        }
        stage('Deploy Image') {
	  steps{
            script {
              docker.withRegistry('',registryCredential){
                registry.push('latest')
              }
            }
          }        
        }
    }
}
