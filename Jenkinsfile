node('docker-agent') {
    timestamps {
        try {
            stage('SCM') {
                git branch: "master", url: "git@github.com:dzottola/dockertestwebapp.git"
            }

	        stage('Docker build image from github') {
                sh "docker build -t dockerwebapp ."
            }

			stage('Docker deploy') {
                sh "docker run -d --restart always -p 5000:5000 dockerwebapp"
            }

        } finally {
            cleanWs notFailBuild: false
        }
    }
}
