
pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/matanelkobi/Jenkins.git'
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

