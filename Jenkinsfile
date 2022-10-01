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
        dir("HelloWorld") {
          cmakeBuild(
		installation: 'InSearchPath'
		)
        }
      }
    }
    stage("Test") {
      steps {
        dir("HelloWorld") {
          ctest(
                  installation: 'InSearchPath'
          )
      }
    }
  }
}
