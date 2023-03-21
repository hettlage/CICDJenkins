pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile.python'
    }
  }
  stages {
    stage("Build") {
      steps {
        withEnv(["HOME=${env.WORKSPACE}"]) {
          sh 'ls -l'
          sh 'python -V'
          sh 'pip install -r requirements.txt'
        }
      }
    }
  }
}
