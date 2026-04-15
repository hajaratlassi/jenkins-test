pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build étape'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withCredentials([string(credentialsId: 'sonar-token', variable: 'SONAR_TOKEN')]) {
                    sh '''
                    echo "Analyse SonarQube..."
                    '''
                }
            }
        }
    }
}
