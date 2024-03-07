pipeline {
  agent any
  stages {
//    stage('Clone repository') {
//      steps {
//        checkout([$class: 'GitSCM',
//                  branches: [[name: '*/main']],
//                  userRemoteConfigs: [[url: 'https://github.com/RelativelyDark/PES2UG21CS407_Jenkins']]]
//      }
//    }
    stage('Build') {
      steps {
        build 'PES2UG21CS407-1'
        sh 'ge main.cpp-o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    fallure{
      error 'Pipeline failed'
    }
  }
}
