try {
node {
    def app

    stage('Clone Repository')
	git clone https://github.com/kamauwangugi/class-test'
    {
        checkout scm
    }

    stage('Show me the files') {
docker image build --tag docker push dknsaf/dockerimagebuild1:tagname
        sh "ls -l"	
       
    }

stage('Push')
	{
                        docker login --username dknsaf --email=dknsaf@gmai.com
                        docker push /dockerimagebuild1
                }



 stage('Deploy'){
                        docker run dockerimagebuild1
                }


}
 /*****************************************
 * To use this function you need to install
 * the Slack Notification Plugin
 ****************************************/

def notifySlack(additionalInfo = '') {
    def colorCode = '#79ae40'
    def status = 'SUCCESS'
    if (currentBuild.result == 'FAILURE') {
        colorCode = '#d34e56'
        status = 'FAILURE'
    }
    if (currentBuild.result == 'ABORTED' ) {
        colorCode = '#938d8e'
        status = 'ABORTED'
    }
    def commitText = sh(returnStdout: true, script: 'git show -s --format=format:"*%s*  _by %an_" HEAD').trim()
    def subject = "${env.JOB_NAME} - #${env.BUILD_NUMBER} ${status} (<${env.BUILD_URL}|Open>)"
    def summary = "${subject}\nChanges: ${commitText}\nBranch: ${env.GIT_BRANCH}\n${additionalInfo}"
    slackSend channel: "${env.SLACK_CHANNEL}", color: colorCode, message: summary, teamDomain: "${env.SLACK_TEAM_DOMAIN}", token: "${env.SLACK_TOKEN}"
}
