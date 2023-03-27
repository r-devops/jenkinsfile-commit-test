pipeline {
    agent any 

    stages {

        stage('Build Name') {
            steps {
                sh 'env'
                script {
                    def replayClassName = "org.jenkinsci.plugins.workflow.cps.replay.ReplayCause​"
                    def isReplay = currentBuild.rawBuild.getCauses().any{ cause -> cause.toString().contains(replayClassName) }
                    print isReplay
                }
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
