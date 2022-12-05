node{
    stage("Pull Source Code from GitHub"){
    git branch: 'devops', url: 'https://github.com/tabrezid54/devops.git'
    }
    stage("list"){
        sh 'ls -ltr'
    }
    stage("workdir"){
        sh 'pwd'
    }
    stage("user"){
        sh 'whoami'
    }
}
