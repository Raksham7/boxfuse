pipeline {
    agent any 
    stages{
        stage("Checkout"){
            steps{
                git credentialsId: 'git', url: 'https://github.com/Raksham7/boxfuse.git'
            }
        }
        stage("Testing"){
            steps{
                sh 'mvn clean test' 
            }
        }
        stage('Integration Testing'){
            steps{
                sh 'mvn clean verify -DskipUnitTests'
            }
        }
    }
}      
