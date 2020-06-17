pipeline {
  agent any
  //tools {
    //maven “Maven”
  //}
  stages {
      stage("build") {
          steps {
            echo 'build'
              snDevOpsStep()
            sleep 5
              //sh ‘mvn clean install’
          }
      }
      stage("test") {
           steps {
             echo 'test'
                snDevOpsStep()
             sleep 5
                sh 'mvn test -Dpublish'
                junit '**/target/surefire-reports/*.xml'
           }
       }
    
     stage("prod") {
          steps {
            echo 'Prod'
            snDevOpsStep()
            sleep 5
            snDevOpsChange()
          }
      }
    
      stage("deploy") {
          steps {
            echo 'Deploying..'
            snDevOpsStep()
            sleep 5
            //snDevOpsChange()
          }
      }
  }
}
