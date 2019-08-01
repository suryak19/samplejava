pipeline {
   agent any
    options {
        skipDefaultCheckout()
    }
   tools {
      maven "maven"
   }
   
   stages {
       stage("build") {
           steps {
               snDevOpsStep '8b80be30c7c33300b8e302b827c26005'
               echo "Building"
               sleep 5
           }
       }
       stage("test1") {
           steps {
               snDevOpsStep '0b80be30c7c33300b8e302b827c26005'
               sh "mvn clean install"
               echo "Testing"
               sleep 3
           }
       }
       stage("deploy") {
           steps {
               snDevOpsStep '0380be30c7c33300b8e302b827c26005'
               snDevOpsChange()
               echo "Deploying"
               sleep 7
           }
       }
      stage("Post-Build"){
         steps{
               snDevOpsStep '8780be30c7c33300b8e302b827c26005'
               junit '**/target/surefire-reports/*.xml'
            }
      }
   }
   //post {
     // always {
       //  snDevOpsStep '8780be30c7c33300b8e302b827c26005'
        // junit '**/target/surefire-reports/*.xml'
      //}
   //} 
}
