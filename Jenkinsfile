
node('docker-agent') {
    timestamps {
        try {

 stage('SCM') {git branch: "master", url: "git@github.com:dzottola/dockertestwebapp.git"}

            stage('Build & Test') {

                try {
				stage('clean up') {sh "docker container stop build_and_run_webapp_container_vote_1 build_and_run_webapp_container_result_1 redis db"}

                stage('clean up') {sh "docker container rm build_and_run_webapp_container_vote_1 build_and_run_webapp_container_result_1 redis db"}

                stage('Docker deploy') {sh "docker-compose up --build"}



                } finally {
                stage('Docker deploy') {sh "docker-compose up --build"}
                }
            }

        } finally {
            cleanWs notFailBuild: false
        }
    }
}
