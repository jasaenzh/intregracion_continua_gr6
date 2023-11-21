pipeline {
    agent any
    
    stages {
        stage('Clonar Repositorio') {
            steps {
                script {
                    sh 'rm -rf intregracion_continua_gr6'
                    sh 'git clone https://github.com/jasaenzh/intregracion_continua_gr6'
                }
            }
        }
        
        stage('Construir y Publicar Imagen Docker') {
            steps {
                script {
                    sh 'cd intregracion_continua_gr6'
                    sh 'docker build -t integracioncontinua .'
                    //sh 'docker push integracioncontinua'
                }
            }
        }
        
    }
    
    post {
        success {
            echo '¡Despliegue exitoso!'
        }
        failure {
            echo '¡Despliegue fallido!'
        }
    }
}