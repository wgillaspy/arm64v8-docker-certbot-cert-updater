pipeline {

    agent { label 'jenkins-bc-certbot' }

     triggers {
            pollSCM('H */12 * * *')
     }

    stages {
        stage('Prep') {
          steps {

           sh "certbot renew"

          }
        }


    }
}