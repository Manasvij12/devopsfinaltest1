pipeline{
    agent any
    
    tools{
    mvn 'Maven'
    }
    
    stages{
    stage('Checkout'){
    steps{
    git branch:'master, url:'https://github.com/Manasvij12/devopsfinaltest1.git'
    }
  }
    
    stage('Build'){
    steps{
    sh 'mvn clean package'
    }
   }
   
   stage('Test'){
   steps{
   sh 'mvn test'
   }
   }
   
   stage('Run application'){
   steps{
   sh 'java jar target/devopsfinaltest1-1.0-SNAPSHOT.jar'
   }
   }
   }
   post{
   success{
   echo 'build and deployment successful'
   }
   failure{
   echo 'build failed'
   }
   }
   }
   
   



































}
