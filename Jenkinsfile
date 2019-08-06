node {
  
   stage("deploy") {
       snDevOpsStep '4a37621ec7833300b8e302b827c26052'
       snDevOpsChange()
       stage("deploy-nested") {
         echo "Deploying"
         sleep 7
       }
   }
}
