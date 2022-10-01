pipeline {
  agent any
  stages {
    stage("Generate Build System") {
      steps {
          cmakeBuild(
		    installation: 'InSearchPath',
		    buildType: 'Release',
		    generator: 'Unix Makefiles',
		    cleanBuild: true,
		    steps: [[withCmake: true]]
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
