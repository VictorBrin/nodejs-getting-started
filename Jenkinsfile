pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/VictorBrin/nodejs-getting-started'
            }
        }

        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Tests') {
            steps {
                sh 'npm test || echo "Tests fallaron, pero continuo con el pipeline"'
            }
        }

        stage('Run application') {
            steps {
                sh 'nohup npm start &'
            }
        }
    }
}
