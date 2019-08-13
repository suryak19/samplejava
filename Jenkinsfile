node {
   
   stage("Checkout scm") {
      checkout scm
   }
   
   stage("build") {
       snDevOpsStep '7dd16550c7173300b8e302b827c260c3'
       echo "Building1" 
       sh 'mvn clean install'
       
   }
   stage("test") {
       snDevOpsStep 'f9d16550c7173300b8e302b827c260c3'
       echo "Testing"
       sh 'mvn test -Dpublish'
       
       junit '**/target/surefire-reports/*.xml' 
   }
   
}
