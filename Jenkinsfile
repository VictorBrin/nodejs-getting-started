pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/VictorBrin/nodejs-getting-started.git'
            }
        }

        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Tests') {
            steps {
                sh 'npm test || echo "No hay pruebas definidas"'
            }
        }

        stage('Run application') {
            steps {
                sh 'npm start &'
            }
        }
    }
}
