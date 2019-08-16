pipeline {
   agent any
   stages {
       stage("build") {
           steps {
               //snDevOpsStep '80478221c7d33300b8e302b827c260b5'
               echo "Building"
               sleep 5
           }
       }
       stage("test") {
           steps {
               snDevOpsStep '00478221c7d33300b8e302b827c260b5'
               echo "Testing"
               sleep 3
           }
       }
       stage("deploy") {
           steps {
               snDevOpsStep '08478221c7d33300b8e302b827c260b4'
               echo "Deploying"
               sleep 7
           }
       }
       stage("prod") {
           steps {
               snDevOpsStep '8c478221c7d33300b8e302b827c260b4'
              snDevOpsChange()
               echo "production"
               sleep 7
           }
       }
   }
}
