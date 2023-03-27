def isBuildAReplay() {
  // https://stackoverflow.com/questions/51555910/how-to-know-inside-jenkinsfile-script-that-current-build-is-an-replay/52302879#52302879
  def replyClassName = "org.jenkinsci.plugins.workflow.cps.replay.ReplayCause"
  currentBuild.rawBuild.getCauses().any{ cause -> cause.toString().contains(replyClassName) }
}

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
