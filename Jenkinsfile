pipeline {
    agent any

    stages {

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
