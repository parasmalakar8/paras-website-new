pipeline {
    agent any
    stages {
        stage('Build Image') {
            steps {
                sh 'docker build -t paras-website-new .'
            }
        }
        stage('Run Website') {
            steps {
                sh 'docker rm -f paras-site || true'
                sh 'docker run -d --name paras-site -p 8082:80 paras-website-new'
            }
        }
    }
}
