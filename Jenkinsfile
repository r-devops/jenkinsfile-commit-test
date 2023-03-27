pipeline {
    agent any 

    stages {

        stage('test') {
            steps {
                sh 'env'

                script {
                    currentBuild.displayName = GIT_COMMIT
                }
            }

        }

    }
    post {
        always {
           cleanWs() 
        }
    } 


}



