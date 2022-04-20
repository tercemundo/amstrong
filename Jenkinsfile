pipeline {
    agent any

    stages {
        stage('Obtener el repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/alfonsoalba-cursos/openwebinars-curso-de-jenkins.git'
            }
        }
        stage('Construir la documetación') {
            steps {
                sh "doxygen"
            }
            
        }
    }
    post {
        success {
            publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: 'html/', reportFiles: 'files.html', reportName: 'Documentación', reportTitles: ''])
        }
    }
}
