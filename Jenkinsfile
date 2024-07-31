pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', credentialsId: '03bd3853-dacd-457d-9f20-527c2035cbb7', url: 'https://github.com/MatanElkobi/Jenkins.git'
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
