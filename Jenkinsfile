pipeline {
    agent any 

    stages {

        stage('Build Name') {
            when {
    expression { jenkins.isBuildAReplay() }
  }
            steps {
                sh 'env'
            }
        }

        stage('test') {
            steps {
                sh 'env'

                // script {
                //     currentBuild.displayName = GIT_COMMIT
                // }
            }

        }

    }
    post {
        always {
            script {
                    currentBuild.displayName = GIT_COMMIT
                }
           cleanWs() 
        }
    } 


}
