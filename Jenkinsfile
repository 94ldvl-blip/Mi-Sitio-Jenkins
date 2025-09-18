pipeline {
    agent any

    stages {
        stage('Clonar repositorio') {
            steps {
                git 'https://github.com/94ldvl-blip/Mi-Sitio-Jenkins.git'
            }
        }

        stage('Copiar archivos al contenedor web') {
            steps {
                sh 'docker cp index.html web-server:/usr/share/nginx/html/index.html'
            }
        }

        stage('Finalizado') {
            steps {
                echo '🚀 Sitio desplegado exitosamente con Jenkins.'
            }
        }
    }
}
