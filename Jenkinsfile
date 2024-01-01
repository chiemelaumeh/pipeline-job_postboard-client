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
        
            }
        }
        stage("Publish Artifacts") {
            steps {   
            sh "set +x && echo \"//ec2-18-219-224-215.us-east-2.compute.amazonaws.com:8081/repository/nexus-postboard-client/:_authToken=NpmToken.d7cc2907-ecf0-3922-88ef-b76f1bd96f33\" >> .npmrc"
            sh "npm publish"
            }
        }
          }
         }
