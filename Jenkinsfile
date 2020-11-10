pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is the build job for lagairogo-shopping-cart'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'this is the test job for lagairogo-shopping-cart'
        sh 'mvn test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the package job for lagairogo-shopping-cart'
        sh 'mvn package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'maven'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}