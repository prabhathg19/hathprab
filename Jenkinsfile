cat <<EOF > Jenkinsfile
pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git url: 'https://github.com/YOUR_USERNAME/hello-docker-jenkins.git', branch: 'main'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t hello-jenkins .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run --rm hello-jenkins'
            }
        }
    }
}
EOF
