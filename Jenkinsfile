node('docker-agent') {
    timestamps {
        try {
            stage('SCM') {
                git branch: "master", url: "git@github.com:dzottola/dockertestwebapp.git"
            }

			stage('Docker deploy') {
                sh "docker-compose up"
            }

        } finally {
            cleanWs notFailBuild: false
        }
    }
}
