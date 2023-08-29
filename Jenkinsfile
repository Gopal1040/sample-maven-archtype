pipeline {
agent {
  label {
    label 'jenkins_slave'
  }
}
stages {
  stage('Checkout') {
    steps {
      checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github_credentials', url: 'https://github.com/devopsdeepdive/sample-maven-archtype.git']])
    }
  }

}
}
