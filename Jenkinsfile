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
                        docker login --username dknsaf --email=dknsaf@gmail.com
                        docker push /dockerimagebuild1
                }



 stage('Deploy'){
                        docker run dockerimagebuild1
                }



