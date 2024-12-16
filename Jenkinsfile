pipeline {
    agent any
    stages {
        stage('Code Analysis') {
            steps {
                withSonarQubeEnv('SonarQubeServer') {
                    sh '''
                    sonar-scanner \
                        -Dsonar.projectKey=sonarqube-demo \
                        -Dsonar.sources=src \
                        -Dsonar.host.url=http://3.99.178.3:9000 \
                        -Dsonar.login=admin
                    '''
                }
            }
        }
    }
}

