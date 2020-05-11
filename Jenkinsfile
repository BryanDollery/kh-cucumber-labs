pipeline {
  agent {
    docker {
      image 'bryandollery/maven-repo'
    }

  }
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/BryanDollery/kh-cucumber-labs.git', branch: '*/master')
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean compile'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Release') {
      steps {
        echo 'Released'
      }
    }

  }
}