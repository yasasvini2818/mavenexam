pipeline{
   agent any
   tools{
   maven 'Maven'
  }
  stages{
     stage('Checkout')
     {
        git branch:'master' url:'https://github.com/yasasvini2818/mavenexam.git'
     }
     stage('Build')
     {
        sh 'mvn clean package'
     }
     stage('Test')
     {
        sh 'mvn test'
     }
     stage('Run Application')
     {
         sh 'java -jar target/MyMavenApp8-1.0-SNAPSHOT.jar'
     }
  }
  post
  {
    success{
       echo 'Build successful'
       }
       failure{
         echo 'Build failed'
        }
       }
      }
