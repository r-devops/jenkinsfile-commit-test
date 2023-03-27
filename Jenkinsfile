pipeline {
    agent any 

    stages {

        stage('test') {
            steps {
                env
            }

        }

    }
    post {
        always {
           cleanWs() 
        }
    } 


}



