pipeline {
  agent any
   tools {
        maven "M2_HOME"
        jdk "JDK"
    }
  stages {
    stage('Git Check out') {
      steps{
         git branch: 'main', url: 'https://github.com/Ranjithvavilla/Junit.git'
      }
    }
    stage('UNIT testing') {
      steps{
         sh 'mvn test'
      }
    }
  }
}
