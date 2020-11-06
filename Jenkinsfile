pipeline {
    agent {
        docker {
            image 'maven:3.6.3'
            args '-v $HOME/.m2:/root/.m2'
        }
    }
    stages {
        stage('build') {
            steps {
                //checkout scm
                git url: 'git://github.com/zhxdong95/simple-web.git', branch: 'main'
                //sh 'cd simple-web'
                //sh 'mvn --version'
                //git 'https://github.com/zhxdong95/simple-web.git'
                sh 'mvn clean package'
            }
        }
    }
}