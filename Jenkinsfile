pipeline { 
     agent docker { image 'node:latest' }
  
   stages {
   
     stage('Node Version') { 
        steps { 
           sh 'node -version' 
        }
     }
     stage('Install Dependencies') { 
        steps { 
           sh 'npm install' 
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

   }
