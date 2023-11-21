pipeline {
    agent any
    
    stages {
        // stage('Clonar Repositorio') {
        //     steps {
        //         // git clone 'https://github.com/jasaenzh/intregracion_continua_gr6'
        //         git --version
        //     }
        // }
        
        stage('Construir y Publicar Imagen Docker') {
            steps {
                script {
                    // def dockerImage = docker.build('integracion-continua-gr6:version1')
                    // dockerImage.push()
                    sh "dir"
                }
            }
        }
        
        // stage('Desplegar Aplicación') {
        //     steps {
        //         // Agrega pasos para el despliegue según sea necesario
        //     }
        // }
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