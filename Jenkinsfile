pipeline {
  agent any
  stages {
    stage("Build") {
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
    stage("Test") {
      steps {
          ctest(
                  installation: 'InSearchPath'
          )
    }
  }
}
}
