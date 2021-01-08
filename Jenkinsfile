pipeline {
  agent any
  //options {
    //disableResume()
  //}
    stages {
        stage('build') {
            steps {
                echo 'build …'
                 //snDevOpsStep()
                 snDevOpsChange()
            }
        }
        stage('test') {
            steps {
                echo 'test …'
                 //snDevOpsStep()
              snDevOpsChange()
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
