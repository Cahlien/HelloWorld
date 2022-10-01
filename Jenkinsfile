pipeline {
  agent any
  stages {
    stage("Build") {
      steps {
          cmakeBuild(
		installation: 'InSearchPath'
		)
      }
    }
    stage("Test") {
      steps {
          cmakeTest(
                  installation: 'InSearchPath'
          )
    }
  }
}
}
