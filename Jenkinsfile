pipeline {
  agent any
   tools {
        maven "M2_HOME"
        jdk "JAVA_HOME"
    }
  stages {
    stage('Git Check out') {
      steps{
         git branch: 'main', url: 'https://github.com/Ranjithvavilla/Junit.git'
      }
    }
    stage('UNIT testing') {
      steps{
         bat 'mvn clean compile'
      }
    }
     stage('Integration Test') {
      steps{
         bat 'mvn verify -DskiUnitTests'
      }
    }
  }
}
