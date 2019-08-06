pipeline {
   agent any
   stages {
       stage("build") {
           steps {
               snDevOpsStep 'c237621ec7833300b8e302b827c26053'
               echo "Building"
               sleep 5
           }
       }
       stage("test") {
           steps {
               snDevOpsStep '4237621ec7833300b8e302b827c26053'
               //sh "mvn clean install"
               echo "Testing"
               sleep 3
           }
       }
       stage("deploy") {
           steps {
               snDevOpsStep '4a37621ec7833300b8e302b827c26052'
               //snDevOpsChange()
               echo "Deploying"
               sleep 7
           }
       }
   }
}
