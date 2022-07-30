pipeline{
    agent any
    stages{
        stage('validate'){
            steps{
                bat "mvn validate"
            }
        }        
        stage('maven compile'){
            steps{
                bat "mvn compile"
            }
        }
        stage('test'){
            steps{
                bat "mvn test"
            }
        }
        stage('package'){
            steps{
                bat "mvn package"
            }
        }
        stage('verify'){
            steps{
                bat "mvn verify"
            }
        }
         stage('install'){
            steps{
                bat "mvn install"
            }
        }         
    }
}
