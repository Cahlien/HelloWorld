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
          buildType: 'Release',
          sourceDir: '.',
          buildDir: 'build',
          targets: 'all'
        )
    stage("Test") {
      steps {
          ctest(
                  installation: 'InSearchPath'
          )
    }
  }
}
}
