pipeline {
<<<<<<< HEAD
  environment {
    registry = 'akkafranck/nuvola'
    registryCredential = 'akkafranck'
  }
=======
>>>>>>> 88f1ef435c27ec027238ba2a63b70cca37eed365
    agent any
    stages {
        stage('Build_Docker_Image') {
            steps {
<<<<<<< HEAD
                sh 'docker build -t nuvola:2.0 .'
            }
        }
        stage(Deploy Image') {
	  steps{
            script {
              docker.withRegistry('',registryCredential){
                dockerImage.push()
              }
            }
          }        
        }
=======
                sh 'docker build -t nuvola:1.0 .'
            }
        }
>>>>>>> 88f1ef435c27ec027238ba2a63b70cca37eed365
    }
}
