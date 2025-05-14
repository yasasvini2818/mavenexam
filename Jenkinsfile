pipeline{
   agent any
   tools{
   maven 'Maven'
   jdk 'JDK11'
  }
  stages{
     stage('Checkout')
     {
       steps{
        git branch:'master',url:'https://github.com/yasasvini2818/mavenexam.git'
     }
     }
     stage('Build')
     {
       steps{
        sh 'mvn clean package'
     }
     }
     stage('Test')
     {
       steps{
        sh 'mvn test'
     }
     }
     stage('Run Application')
     {
        steps{
         sh 'java -jar target/MyMavenApp8-1.0-SNAPSHOT.jar'
     }
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
