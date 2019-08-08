node {
   stage("build") {
       snDevOpsStep '6d8cb103c7c33300b8e302b827c2603e'
       echo "Building" 
       sh 'mvn clean install'
       
   }
   stage("test") {
       snDevOpsStep 'e98cb103c7c33300b8e302b827c2603e'
       echo "Testing"
       sh 'mvn test -Dpublish'
       
       junit '**/target/surefire-reports/*.xml' 
   }
   
}
