node {
  
   stage("deploy") {
       snDevOpsStep '4a37621ec7833300b8e302b827c26052'
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
}
