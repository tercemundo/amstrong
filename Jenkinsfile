pipeline {
    agent any

    stages {
        stage('Obtener el repositorio') {
            steps { 
                 sh 'git clone https://github.com/tercemundo/amstrong.git'
            }
        }
        

        
        
        
        stage('Tests unitarios') {
            steps {
                sh 'make'
                sh 'make tests-xml'
                junit 'reports/cmocka/*.xml'
            }
        }
    }
    
}
