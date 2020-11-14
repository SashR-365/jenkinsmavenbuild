pipeline{

    agent any

    tools{
    maven 'm3'
    jdk 'jdk8'
    }

    stages{
        stage('Checkout'){
            steps{
                git 'https://github.com/Sash-R 365/jenkinsmavenbuild'
        }
        stage('Compile'){
            steps{
                sh 'mvn clean compile'
            }
        }   
        stage('Test'){
                sh 'mvn clean test'
            }    
        }
        stage('Package'){
            steps{
                sh 'mvn clean package'
            }
        stage('ArchiveArtifact'){
            steps{
                archiveArtifacts 'target/*.jar'
            }
        }    
        }   


    }


}
