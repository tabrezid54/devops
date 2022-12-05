node("my-node"){
    stage("Pull Source Code from GitHub") {
    git branch: 'devops', url: 'https://github.com/tabrezid54/devops.git'
    }
    stage("Create docker image") {
        sh 'docker build -t $JOB_NAME docker/.'
    }
      stage("Delete all docker container") {
        sh 'docker rm -f $(docker ps -aq)'
    }
    stage("Create docker container") {
        sh 'docker run -d --name $JOB_NAME -p 80:80'
    }
}
