pipeline { 
     agent {
  docker { image 'node:latest' }
     }
   stages {
     stage('Checkout SCM') { 
        steps { 
           checkout([$class: 'GitSCM', branches: [[name: '*/dev']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/vishnulal210897/Multibranch-demo.git']]])
        }
     }
        
     stage('Setup') { 
        steps { 
           sh 'node --version' 
        }
     }
     stage('Unit Test') { 
        steps { 
           sh 'echo "Unit testing Application..."'
        }
      }
         stage("Deploy nodejs application") { 
         steps { 
           sh 'echo "deploying application..."'
         }
     }
   	}
   post {
    always {
      cleanWs()
    }
  }
   }
