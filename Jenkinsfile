pipeline {
  agent {
    dockerfile {
      filename 'Dockerfile.python'
    }
  }
  stages {
    stage("Build") {
      steps {
        echo "Result from last build: $UPSTREAM_RESULT"
        echo "Last build number: $UPSTREAM_NUMBER"
        withEnv(["HOME=${env.WORKSPACE}"]) {
          sh 'ls -l'
          sh 'python -V'
          sh 'pip install -r requirements.txt'
        }
      }
    }
  }
}
