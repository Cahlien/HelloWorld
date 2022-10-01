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
        cmake(
          installation: 'InSearchPath',
          arguments: '-DCMAKE_BUILD_TYPE=Release -DCMAKE_BINARY_DIR=cmake-build-release'
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
