pipeline {
   agent any
    options {
        skipDefaultCheckout()
    }
   stages {
       stage("build") {
           steps {
               snDevOpsStep '6370eb90c7073300b8e302b827c260cc'
               echo "Building"
               sleep 5
           }
       }
       stage("test") {
           steps {
               snDevOpsStep 'ef70eb90c7073300b8e302b827c260cb'
               //sh "mvn clean install"
               echo "Testing"
               sleep 3
           }
       }
       stage("deploy") {
           steps {
               snDevOpsStep 'd770eb90c7073300b8e302b827c260cb'
               snDevOpsChange()
               echo "Deploying"
               sleep 7
           }
       }
   }
   post {
      always {
         snDevOpsStep '6f70eb90c7073300b8e302b827c260cb'
        //junit '**/target/surefire-reports/*.xml'
      }
   } 
}
