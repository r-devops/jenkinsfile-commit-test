

pipeline {
    agent any 

    stages {

        stage('Build Name') {
            // when {
            //     expression { jenkins.isBuildAReplay() }
            // }
            steps {
                sh 'env'
                script {
                def replyClassName = "org.jenkinsci.plugins.workflow.cps.replay.ReplayCause"
  currentBuild.rawBuild.getCauses().any{ cause -> cause.toString().contains(replyClassName) }
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
