pipeline {

    agent { label 'jenkins-bc-certbot' }

     triggers {
            cron('H 1 * * *')
     }

    stages {
        stage('Prep') {
          steps {

           sh "certbot renew"

          }
        }


    }
}