pipeline {
    agent any
  
    stages {
      stage('checkout'){
        steps {
          git branch: 'main', url: 'https://github.com/1mrvincent/qa-vat-calculator'
        }
      }
        
        stage ('Sonar Qube Analysis'){
          environment {
            scannerHome = tool 'sonarqube'
          }
            steps{
                withSonarQubeEnv('sonar-qube-1'){
                  sh "${scannerHOme}/bin/sonar-scanner"
                }
            }
        }
    }
}
