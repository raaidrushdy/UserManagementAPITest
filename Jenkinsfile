pipeline {
    agent any
         }
stages {
  stage('Code Quality Analysis') {
            steps {
                echo 'Analyzing code with SonarQube...'
                withSonarQubeEnv('MySonarQubeServer') {
                    sh 'mvn sonar:sonar -Dsonar.projectKey=user-management-api -Dsonar.projectName="User Management API"'
                }
            }
        }
}
