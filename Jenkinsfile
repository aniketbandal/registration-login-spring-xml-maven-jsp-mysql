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
             stage('deploy on browser stage')
        {
            steps{
            bat "Move C:\Program Files (x86)\Jenkins\workspace\testpipeline\target\account-1.0-SNAPSHOT  C:\Program Files\Apache Software Foundation\Tomcat 9.0\webapps\"
            }
        }
            
    }
    
}
