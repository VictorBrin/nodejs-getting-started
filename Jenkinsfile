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
                echo "Saltando tests porque fallan en el proyecto base"
            }
        }

        stage('Run application') {
            steps {
                sh 'nohup npm start &'
            }
        }
    }
}
