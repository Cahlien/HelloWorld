pipeline {
  agent any
  stages {
    stage("Clean") {
      steps {
        deleteDir()
      }
    }
    stage("Clone Repo") {
      steps {
        sh "git clone https://github.com/cahlien/HelloWorld.git"
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
          cmakeTest(
                  installation: 'InSearchPath'
          )
      }
    }
  }
}
