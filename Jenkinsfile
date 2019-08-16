node {
  stage("build") {
      snDevOpsStep '80478221c7d33300b8e302b827c260b5'
      echo "Building"
      sh 'mvn clean install'

  }
  stage("test") {
      snDevOpsStep '00478221c7d33300b8e302b827c260b5'
      echo "Testing"
      sh 'mvn test -Dpublish'

      junit '**/target/surefire-reports/*.xml'
  }

}
