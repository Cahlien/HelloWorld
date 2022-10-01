pipeline {
  agent any
  stages {
    stage("Generate Build System") {
      steps {
          cmakeBuild(
		    installation: 'InSearchPath'
          )
      }
    }
    stage("Build") {
      steps {
        dir("HelloWorld") {
          cmake(
            installation: 'InSearchPath',
          )
        }
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
