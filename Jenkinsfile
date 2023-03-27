pipeline {
    agent any 

    stages {

        stage('test') {
            steps {
                echo 'hai'
            }

        }

    }
    post {
        always {
           cleanWs() 
        }
    } 


}

