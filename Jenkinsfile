pipeline {
    agent any

    stages {
        stage('Obtener el repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/tercemundo/amstrong'
            }
        }
        
        stage('Tests unitarios') {
            steps {
                sh 'make tests-xml'
                junit 'reports/cmocka/*.xml'
            }
        }
    }
  
}
