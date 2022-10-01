pipeline {
  agent any
  stages {
    stage("Generate Build System") {
      steps {
          cmakeBuild(
		    installation: 'InSearchPath',
		    '-DCMAKE_BUILD_TYPE=Release'
          )
      }
    }
    stage("Build") {
      steps {
        cmake(
          installation: 'InSearchPath',
          arguments: '--install'
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
