pipeline{
  agent any
  stages{
    stage (' git checkout') {
      steps{
       git credentialsId: '7ab093af-adaf-4f2c-be1b-ff970aafa032', url: 'https://github.com/Shrveenpk/hello-world.git' 
      }
    }
    stage (' unit testing') {
      steps{
       sh 'mvn test' 
      }
    }
    stage (' integration testing') {
      steps{
       sh 'mvn verify -DskipUnitTests' 
      }
    }
  }
}
