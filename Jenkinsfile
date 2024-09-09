pipeline {
    agent any
    tools {
        maven 'Maven' // Ensure the Maven installation is properly set in Jenkins under Global Tool Configuration
    }
    environment {
        SONARQUBE_SERVER = 'MySonarQubeServer'  // Update this with the SonarQube server name you set in Jenkins
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
}
