@Library('shared-lib')_
pipFunc() {
    git 'http://admin@dnbpuls.sndevops.net:81/scm/dnbpul/dnb-web.git'
    def mvn_version = 'Maven'
    stage('compile') {
        snDevOpsStep (stepSysId:'2736f1d0c70400108c2c02b827c26056')
        printBuildinfo {
        	name = "Compiling..."
        }
        //withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {
        	//sh 'mvn clean install -DskipTests'
		//}
    }
	test()
}
