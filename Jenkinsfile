pipeline{
    agent any
  tools {
      maven 'maven'
  }
    stages {
        stage('compile stage')
        {
            steps{
            bat "mvn clean compile"
            }
        }
        stage('test stage')
        {
            steps{
            bat "mvn test"
            }
        }
        stage('package stage')
        {
            steps{
            bat "mvn package"
            }
        }
 
  
            
    }
    
}
