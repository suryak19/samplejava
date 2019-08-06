node {
  
   stage("deploy") {
       snDevOpsStep '4a37621ec7833300b8e302b827c26052'
        stage("test-nested") {
         echo "Testing nested"
         sleep 7
         stage("test-nestedx2") {
            echo "Testing nested 2"
            sleep 2
         }
       }
   }
}
