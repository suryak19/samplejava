node {
   stage("build") {
       snDevOpsStep 'c237621ec7833300b8e302b827c26053'
       parallel 'build-nested1': {
           stage('build-nestedA') {
               echo "building nested A"
               sleep 3
           }
       }, 'build-nested2': {
           stage('build-nestedB') {
               echo "building nested B"
               sleep 2
           }
       }
   }
   stage("test") {
       snDevOpsStep '4237621ec7833300b8e302b827c26053'
       echo "Testing"
       stage("test-nested") {
         echo "Testing nested"
         sleep 7
         stage("test-nestedx2") {
            echo "Testing nested 2"
            sleep 2
         }
       }
   }
   stage("deploy") {
       snDevOpsStep '4a37621ec7833300b8e302b827c26052'
       stage("deploy-nested") {
         echo "Deploying"
         sleep 7
       }
   }
}
