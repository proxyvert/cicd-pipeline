pipeline {
  agent {
    docker {
      image 'node:18'
    }

  }
  stages {
    stage('checkout scm') {
      steps {
        git(url: 'https://github.com/proxyvert/cicd-pipeline.git', branch: 'main')
      }
    }

    stage('build app') {
      steps {
        sh '''chmod +x ./scripts/build.sh
./scripts/build.sh'''
      }
    }

  }
}