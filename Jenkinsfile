pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
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
                script {
                    echo 'Ejecutando script de prueba en Python...'
                    sh '. venv/bin/activate && python3 -m pytest'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh 'echo "Algo"'
                    // Aquí podrías agregar cualquier paso de limpieza si es necesario
                }
            }
        }
    }
}

