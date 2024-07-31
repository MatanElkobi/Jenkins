
pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-username/your-repo.git'
            }
        }
        stage('Run Docker Image') {
            steps {
                script {
                    def dockerImage = docker.image('hello-world')
                    dockerImage.pull()
                    dockerImage.run()
                }
            }
        }
    }
}

