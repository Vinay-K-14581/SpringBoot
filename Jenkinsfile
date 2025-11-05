pipeline {
  agent any
  tools {
    maven 'Maven 3.9.11'
    // jdk 'JDK 17' // uncomment if you have a configured JDK tool
  }

  stages {
    stage('Build') {
      steps {
        echo 'compile maven app'
        sh 'mvn -B -V clean compile'
      }
    }
    stage('Test') {
      steps {
        echo 'test maven app'
        sh 'mvn -B test'
      }
    }
    stage('Package') {
      steps {
        echo 'package maven app'
        sh 'mvn -B -DskipTests package'
      }
    }
  }

  post {
    always { echo 'This pipeline is completed..' }
  }
}
