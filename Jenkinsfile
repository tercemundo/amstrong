pipeline {
    agent any

    
        
        stage('Tests unitarios') {
            steps {
                sh 'make tests-xml'
                junit 'reports/cmocka/*.xml'
            }
        }
    }
  
}
