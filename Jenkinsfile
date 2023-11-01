pipeline { 
    
    agent any
    
    stages {
        stage("Checkout"){
            steps { 
                checkout scm
            }
        }
        stage("Code coverage") { 
            steps {
                jacoco() 
                
            } 
           }

        stage("Build") {
            steps {   
            sh "npm install"  
            // sh "nodemon server.js"
            }
        }
          }
         }
