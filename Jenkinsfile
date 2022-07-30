pipeline{
    agent any
//    environment {
  //      PATH = "$PATH:C:\DevTools\apache-maven-3.8.5\bin"
   // }
    stages{
       stage('GetCode'){
            steps{
                git 'https://github.com/TanujaSalunke/java_LoginApp.git'
            }
         }        
  //     stage('Build'){
    //        steps{
      //          sh 'mvn clean package'
        //    }
       //  }
        stage('SonarQube analysis') {
//    def scannerHome = tool 'SonarScanner 4.0';
        steps{
        withSonarQubeEnv('sonarqube-9.5') { 
        // If you have configured more than one global server connection, you can specify its name
//      sh "${scannerHome}/bin/sonar-scanner"
        sh "mvn sonar:sonar"
    }
        }
        }
     }
}
