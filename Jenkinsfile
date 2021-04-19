def artifactName = "ppm-jar" // also used for nexus filePath and artifactId attributes
def artifactVersion = "5.${env.BUILD_NUMBER}"
def artifactSemVersion = "${artifactVersion}.0"
def repoName = "ppm-repo"
pipeline {
    agent any
    tools { 
        maven 'Maven' 
    }
    stages {
        stage('CI') {
            steps {
              echo 'running CI'
              sh 'mvn compile'
              sh 'mvn verify'
        	}
            post {
                always {
                    junit '**/target/surefire-reports/*.xml' 
                }
            }
        }
        stage('UAT deploy') {
            steps {
		            echo 'running UAT deploy'
                sh 'mvn package'
		            snDevOpsArtifact(artifactsPayload:"""{"artifacts": [{"name": "${artifactName}","version":"${artifactVersion}","semanticVersion": "${artifactSemVersion}","repositoryName": "${repoName}"}]}""")
	    	   }
        }
        stage('UAT test') {
          	steps {
                echo 'running UAT deploy'
                snDevOpsChange()
		        }
        }
	}
}
