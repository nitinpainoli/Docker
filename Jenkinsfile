node() {

   
   stage('Build & Deploy Docker') {
       
        sh '''echo 'hii''''
    }

    stage('Microbadger Webhook') {

        hook = registerWebhook()
        echo "Waiting for POST to ${hook.getURL()}"

        sh  "curl -X POST -d 'OK' \
          https://hooks.microbadger.com/images/stuartshay/microservice-api/zNG1zy7qGd0StURmg-lhGKA0XAE="
        
        data = waitForWebhook hook
        echo "Webhook called with data: ${data}"
    }


    

}
