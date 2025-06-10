pipeline{
  agent any
  tools{
    maven'Maven'
  }
  stages{
    stage('Checkout'){
      steps{
        git branch:'master',url:'https://github.com/bitcse02/mavenappnewpro.git'
      }
    }
    stage('Build'){
      steps{
        sh'mvn clean install'
      }
    }
    stage('Test'){
      steps{
        sh'mvn test'
      }
    }
    stage('Run'){
      steps{
        sh'java -jar target/MyMavenApp1-1.0-SNAPSHOT.jar'
      }
    }
  }
  post{
    success{
      echo'Build success'
    }
    failure{
      echo'Build failure'
    }
  }
}

