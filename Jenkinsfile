pipeline {
    agent any 
     currentBuild.result = "SUCCESS"
 try {

    stages {
       stage('Checkout'){

          checkout scm
        }
        stage('Build Docker'){

            print "Build Docker"
       }
        
      stage('Test'){

         env.NODE_ENV = "test"

         print "stage Test"
       }

       stage('Push'){

          print "Push Docker"
       }

       stage('Deploy') {
            steps {
                sh 'echo  "Deploy"'
            }
        }
       stage('Cleanup'){

         print "Cleanup"
       }
    }
    }
    catch (err) {

        currentBuild.result = "FAILURE"

        throw err
    }

    
}

