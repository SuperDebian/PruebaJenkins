pipeline {
    agent any

    stages {
        stage('Preparar entorno') {
            steps {
                script {
                    // Instalar dependencias necesarias, incluyendo tree
                    echo 'Preparando entorno de Python y tree...'
                    sh 'sudo apt-get update && sudo apt-get install -y python3 python3-pip && sudo apt install tree'
                }
            }
        }

        stage('Ejecutar script de prueba') {
            steps {
                script {
                    echo 'Ejecutando script de prueba en Python...'
                    // Asegúrate de que tu script de Python esté en el repositorio o en la ubicación correcta
                    sh 'python3 python.py'
                }
            }
        }

        stage('Limpiar') {
            steps {
                echo 'Limpiando después de la ejecución del script...'
                // Aquí podrías agregar cualquier paso de limpieza si es necesario
            }
        }
    }

    post {
        always {
            echo 'Pipeline completo!'
        }
    }
}
