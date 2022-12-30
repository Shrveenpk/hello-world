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
    stage (' Maven Build') {
      steps{
       sh 'mvn clean install package' 
      }
    }
    stage (' Sonar') {
      steps{
       withSonarQubeEnv(credentialsId: 'cc4d1c9c-23fd-4667-8219-e4d3ca7e17e8') {
        // some block
        } 
      }
    }
  }
}
