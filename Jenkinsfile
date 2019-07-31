pipeline {
   agent any
    options {
        skipDefaultCheckout()
    }
   stages {
       stage("build") {
           steps {
               snDevOpsStep '8d8a11c7dbbee300f16092dadb9619cb'
               echo "Building"
               sleep 5
           }
       }
       stage("test") {
           steps {
               snDevOpsStep '76a381e4c7c33300b8e302b827c260f2'
               //sh "mvn clean install"
               echo "Testing"
               sleep 3
           }
       }
       stage("deploy") {
           steps {
               snDevOpsStep '7ea381e4c7c33300b8e302b827c260f1'
               snDevOpsChange()
               echo "Deploying"
               sleep 7
           }
       }
   }
   //post {
     // always {
       //  snDevOpsStep '6f70eb90c7073300b8e302b827c260cb'
        //junit '**/target/surefire-reports/*.xml'
      //}
   //} 
}
