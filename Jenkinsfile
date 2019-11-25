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
             stage('Organise Files'){                         
         steps{  
                script{                        
                    File sourceFolder = new File("C:\Program Files (x86)\Jenkins\workspace\testpipeline\target\account-1.0-SNAPSHOT");
                    File  destinationFolder = new File("C:\Program Files\Apache Software Foundation\Tomcat 9.0\webapps");                                                   
                    File[] listOfFiles = sourceFolder.listFiles();
                    echo "Files Total: " + listOfFiles.length;  

                    for (File file : listOfFiles) {
                        if (file.isFile()) {
                            echo file.getName()                                                                
                            Files.copy(Paths.get(file.path), Paths.get("C:\Program Files\Apache Software Foundation\Tomcat 9.0\webapps"));                                   
                        }
                    }                  
                }                                
            }                           
        } 
    }
    
}
