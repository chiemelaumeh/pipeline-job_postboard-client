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
            sh "set +x && echo \"//ec2-18-219-84-162.us-east-2.compute.amazonaws.com:8081/repository/postboard-client_hosted/:_authToken=NpmToken.2843eecf-c55f-3155-9788-2091229be97a\" >> .npmrc"
            sh "npm publish"
            }
        }
          }
         }
