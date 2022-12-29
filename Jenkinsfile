pipeline {
    agent any
    stages {
        stage('Git Clone') {
            steps {
                git url: 'https://github.com/vimalsh/project1-php.git', branch: 'main'
            }
        }
        stage('Build'){
            steps {
                sh 'docker build -t 08091993deadly/phpapp:latest .'
            }
        }
        stage('Run'){
            steps {
                sh 'docker run -d -p 80:80 08091993deadly/phpapp:latest'
            }
        }
    }
}