pipeline {

    agent { label 'jenkins-bc-certbot' }

     triggers {
            cron('H 7 * * *')
     }

    stages {
        stage('Prep') {
          steps {

              sh """

                 chmod +x authenticator.sh
                 chmod +x cleanup.sh

              """

              withCredentials([usernamePassword(credentialsId: 'CF_API_USER_PASS', usernameVariable: 'EMAIL', passwordVariable: 'API_KEY')]) {

                  sh "certbot renew --no-random-sleep-on-renew --preferred-challenges=dns --manual-auth-hook ./authenticator.sh --manual-cleanup-hook ./cleanup.sh"
              }

          }
        }


    }
}