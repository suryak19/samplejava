pipeline {
  agent any
  //options {
    //disableResume()
  //}
    stages {
        stage('build') {
            steps {
                echo 'build …'
                //curlCall()
                 snDevOpsStep()
                 //snDevOpsChange()
            }
        }
        stage('test') {
            steps {
                echo 'test …'
                 //snDevOpsStep()
              //snDevOpsChange()
            }
        }
        stage('Deploy for development') {
            when {
                branch 'development'
            }
            steps {
                 snDevOpsStep()
            }
        }
        stage('Deploy for production') {
            when {
                branch 'production'
            }
            steps {
                 snDevOpsStep()
            }
        }
    }

}

def curlCall(){
               def jsonObj = [: ]
               def json = new groovy.json.JsonBuilder(jsonObj)
               def response = ["curl", "-k", "-X", "POST", "-H", "Content-Type: application/json", "-d", "", "http://devops.integration.user:devops@127.0.0.1:8082/api/sn_devops/v1/devops/tool/orchestration?toolType=jenkins&toolId=36a4417dc76120108c2c02b827c260b9"].execute()
               response.waitFor()
               println response.err.text
               println response.text
}
