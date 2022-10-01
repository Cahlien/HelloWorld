pipeline {
  agent any
  stages {
    stage("Clean") {
      steps {
        deleteDir()
      }
    }
    stage("Build") {
      steps {
        dir("HelloWorld2") {
          cmakeBuild(
		installation: 'InSearchPath'
		)
        }
      }
    }
    stage("Test") {
      steps {
        dir("HelloWorld2") {
          ctest(
                  installation: 'InSearchPath'
          )
      }
    }
  }
}
}
