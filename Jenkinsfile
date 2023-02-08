node {
      stage("Git Clone"){

        git branch: 'main', url: 'https://github.com/chanakyad/Configserver.git'
    }
   
    stage("Docker build"){
    sh 'docker build -t configserver:latest -f Dockerfile .'
        sh 'docker image ls'
    }
   stage("Deploy"){
    sh ' docker rm -f configserver:latest||true'
    sh 'docker run -d -p -- name configserver:latest configserver:latest '
}
}
