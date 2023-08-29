pipeline {
agent any
/* agent {
  label {
    label 'jenkins_slave'
  }
} */
stages {
  stage('Checkout') {
    steps {
      checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github_credentials', url: 'https://github.com/devopsdeepdive/sample-maven-archtype.git']])
    }
  }
  stage('Build') {
    steps {
      sh 'mvn compile'
    }
  }
   stage('Test') {
    steps {
      sh 'mvn test'
    }
  }
    stage('Package') {
    steps {
      sh 'mvn package'
    }
  }

}
}
