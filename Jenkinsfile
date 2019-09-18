@Library('shared-lib')_
pipFunc() {
    git 'http://admin@dnbpuls.sndevops.net:81/scm/dnbpul/dnb-web.git'
    def mvn_version = 'Maven'
    stage('compile') {
        snDevOpsStep (stepSysId:'8cbb707adbbbb3003e87f5861d961908')
        printBuildinfo {
        	name = "Compiling..."
        }
        //withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {
        	//sh 'mvn clean install -DskipTests'
		}
    }
}
