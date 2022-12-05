pipeline {
    agent { node { label 'my-node' } }

    stages {
        stage('Pull Source Code from GitHub') {
            steps {
                git branch: 'devops', url: 'https://github.com/tabrezid54/devops.git'
            }
        }
        stage('Create docker image') {
            steps {
                sh 'docker build -t $JOB_NAME docker/.'
            }
        }
        stage('Delete all running docker container') {
            steps {
                sh 'docker rm -f $(docker ps -aq)'
            }
        }
        stage('Create docker container') {
            steps {
                sh 'docker run -d --name $JOB_NAME -p 80:80 $JOB_NAME'
            }
        }
    }
}
