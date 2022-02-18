pipeline { 
     agent {
  docker { image 'node:latest' }
     }
   stages {
   stage('Checkout SCM') { 
        steps { 
           checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/vishnulal210897/Multibranch-demo.git']]])
        }
     }
     stage('Setup') { 
        steps { 
           sh 'node --version' 
        }
     }
     stage('Smoke Test') { 
        steps { 
           sh 'echo "Smoke testing Application..."'
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
