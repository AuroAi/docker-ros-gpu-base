node('docker')  {


    currentBuild.result = "SUCCESS"

    try {

       stage('Checkout'){

          checkout scm
       }

       stage('Test'){

         env.NODE_ENV = "test"

         print "stage Test"

        
       }

       stage('Build Docker'){

            print "Build Docker"
       }

       stage('Push'){

          print "Push Docker"
       }

       stage('Cleanup'){

         print "Cleanup"
       }



    }
    catch (err) {

        currentBuild.result = "FAILURE"

        throw err
    }

}
