node {
    
    stage('Checkout') {
        checkout scm
    }

    stage('Instalar Dependencias') {
        'npm install'
    }

    stage('Construir') {
        'npm run build'
    }

     stage('Docker') {
        'docker build -t angular .'
    }

    
}