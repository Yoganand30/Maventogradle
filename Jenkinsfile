pipeline{
  agent any
  tools{
    maven 'Maven'
  }
  stages{
    stage('Chechout'){
      steps{
        git branch:'master',url:'https://github.com/Yoganand30/Maventogradle.git'
      }
    }
    stage('build'){
      steps{
        sh 'mvn complie pakage'
      }
    }
    stage('test'){
      steps{
        sh 'mvn test'
      }
    }
    stage('run'){
      steps{
        sh 'java -jar build/libs/maventogradle-1.0-SNAPSHOT.jar'
      }
    }
  }
}
