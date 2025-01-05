pipeline {
  agent any
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