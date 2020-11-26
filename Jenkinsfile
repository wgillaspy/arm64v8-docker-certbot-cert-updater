pipeline {

    agent { label 'jenkins-bc-certbot' }

     triggers {
            cron('H 7 * * *')
     }

    stages {
        stage('Prep') {
          steps {

           sh "certbot renew"

          }
        }


    }
}