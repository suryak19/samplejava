pipeline {
   agent any
   stages {
       stage("build") {
           steps {
               //snDevOpsStep '7dd16550c7173300b8e302b827c260c3'
               echo "Building"
               sleep 5
           }
       }
       stage("test") {
           steps {
               snDevOpsStep 'f9d16550c7173300b8e302b827c260c3'
               echo "Testing"
               sleep 3
           }
       }
       stage("deploy") {
           steps {
               snDevOpsStep 'f1d16550c7173300b8e302b827c260c3'
               echo "Deploying"
               sleep 7
           }
       }
       stage("prod") {
           steps {
               snDevOpsStep '79d16550c7173300b8e302b827c260c3'
              snDevOpsChange()
               echo "production"
               sleep 7
           }
       }
   }
}
