pipeline {
    agent any 

    stages {

        stage('test') {
            steps {
                sh 'env'
            }

        }

    }
    post {
        always {
           cleanWs() 
        }
    } 


}



