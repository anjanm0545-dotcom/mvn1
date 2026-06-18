pipeline{
  agent any
  tools{
    maven 'maven'
  }
  stages{
    stage('Checkout'){
      steps{
        git branch: 'main:',
          url:'https://github.com/anjanm0545-dotcom/mvn1.git'
      }
    }
    stage('Build'){
      steps{
        sh 'mvn compile'
      }
    }
    stage('Tset'){
      steps{
        sh 'mvn test'
      }
    }
    stage('Run Aplication'){
      steps{
        sh 'java -jar target/my-maven-1.0-SNAPSHOT.jar'
      }
    }
  }
  post{
    succes{
      echo 'Build and Deploy Sucessfull'
    }
    failure{
      echo 'Build failed'
    }
  }
}
