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
          cmakeBuild(
		installation: 'InSearchPath'
		)
      }
    }
    stage("Test") {
      steps {
          ctest(
                  installation: 'InSearchPath'
          )
    }
  }
}
}
