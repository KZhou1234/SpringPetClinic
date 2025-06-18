pipeline {
    
    agent any
    tools {maven "mavenV3"}
    
    stages{
        
        stage("chenkout"){
            
            steps{
                
                git branch: "main", url: "https://github.com/KZhou1234/SpringPetClinic.git"
            }
        }
        
        stage("build"){
            steps{
                
                sh "mvn compile"
            }
        }
        
        stage("test"){
            steps{
                
                sh "mvn test"
            }
        }
        
        stage("package"){
            steps{
                sh "mvn package"
            }
        }
        
        stage("deploy"){
            steps{
            
            
            sh "java -jar ./target/*.jar"
            }
                
        }
        
    }
}
