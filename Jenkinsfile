//declarative pipeline syntax

pipeline{
    
    agent any
    
    tools{
        maven 'mymaven'
    }
    
    stages{
        
        // stage means a job to jenkins
        stage('Clone the repo')
        {
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        stage('Compile the code'){
            steps{
                sh 'mvn compile'
            }
        }
         stage('Review the code'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
         stage('Test the code'){
            steps{
                sh 'mvn test'
            }
        }
          stage('package the code'){
            steps{
                sh 'mvn package'
            }
        }
    }
}

// no code will be written outsie the pipeline
