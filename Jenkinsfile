pipeline {
  agent any
  
    stages {
        stage(‘build’) {
            steps {
                echo ‘build …’
                 snDevOpsStep()
                 snDevOpsChange()
            }
        }
        stage(‘test’) {
            steps {
                echo ‘test …’
                 snDevOpsStep()
            }
        }
        stage(‘Deploy for development’) {
            when {
                branch ‘development’
            }
            steps {
                 echo ‘dev branch deployment …’
                 snDevOpsStep()
            }
        }
        stage(‘Deploy for production’) {
            when {
                branch ‘production’
            }
            steps {
                echo ‘prod branch deployment …’
                 snDevOpsStep()
            }
        }
    }
