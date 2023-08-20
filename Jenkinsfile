pipeline {
    agent { label "test" }
	environment {
		DOCKERHUB_CREDS=credentials('dockerHub')
	}
    stages{
        stage("Clone Code"){
            steps{
                git url: "https://github.com/AnupamRoy2191/two-tier-flask-app-docker.git", branch: "main"
            }
        }
        stage("Build & Deploy using docker-compose file"){
            steps{
                sh "docker-compose down && docker-compose up -d"
            }
        }
    }

}
