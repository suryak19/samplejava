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
               snDevOpsStep '8d8a11c7dbbee300f16092dadb9619cb'
               echo "Building"
               sleep 5
           }
       }
       stage("test1") {
           steps {
               snDevOpsStep '0d8a11c7dbbee300f16092dadb9619cb'
               sh "mvn clean install"
               echo "Testing"
               sleep 3
           }
       }
       stage("deploy") {
           steps {
               snDevOpsStep '86aa15c7dbbee300f16092dadb961985'
               snDevOpsChange()
               echo "Deploying"
               sleep 7
           }
       }
   }
   post {
      always {
         snDevOpsStep '818a11c7dbbee300f16092dadb9619cb'
         junit '**/target/surefire-reports/*.xml'
      }
   } 
}
