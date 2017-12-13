pipeline {
    agent any 
    currentBuild.result = "SUCCESS"
 try {
        stages {
           stage('Checkout'){
               steps {
                    echo 'Checkout..'
                    checkout scm
                }

            }
            stage('Build Docker'){
                steps {
                    echo 'Building Docker..'
                }
           }

          stage('Test'){

             steps {
                    echo 'Testing..'
                }
           }

           stage('Push'){
                steps {
                    echo 'Pushing Docker..'
                }
            }

           stage('Deploy') {
                steps {
                    sh 'echo  "Deploy"'
                }
            }
           stage('Cleanup'){

               steps {
                    echo 'Cleaning up ..'
                }
           }
        }
    }
    catch (err) {
        currentBuild.result = "FAILURE"
        throw err
    }

    
}

