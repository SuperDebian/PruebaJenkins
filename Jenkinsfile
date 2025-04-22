pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Instalar dependencias necesarias, incluyendo tree
                    echo 'Preparando entorno de Python y tree...'
                    sh '''
                        python3 -m venv venv
                        . venv/bin/activate
                        pip install -r requirements.txt
                    '''
                }
            }
        }

        stage('Test') {
            steps {
                    echo 'Ejecutando script de prueba en Python...'
                    // Asegúrate de que tu script de Python esté en el repositorio o en la ubicación correcta
                    sh '. venv/bin/activate && python3 -m pytest'
                }
            }
        }

        stage('Deploy') {
            steps {
                sh'echo "Algo"'
                // Aquí podrías agregar cualquier paso de limpieza si es necesario
            }
        }
    }
}
