pipeline { 
     agent {
  docker { image 'node:latest' }
     }
   stages {
   
     stage('Node Version') { 
        steps { 
           sh 'node --version' 
        }
     }
     stage('Install Dependencies') { 
        steps { 
           sh 'npm install' 
        }
     }
     stage('Regression Test') { 
        steps { 
           sh 'echo "Regression testing Application..."'
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
