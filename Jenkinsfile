pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Instalar Dependencias') {
            steps {
                script {
                    'npm install'
                }
            }
        }

        stage('Construir') {
            steps {
                script {
                    sh 'npm run build'
                }
            }
        }

        stage('Docker') {
            steps {
                script {
                    sh 'docker build -t angular .'
                }
            }
        }
    }
}
