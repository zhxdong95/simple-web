pipeline {
    agent {
        docker {
            image 'maven:3.6.3-ibmjava-alpine'
            args '-v $HOME/.m2:/.m2'
        }
    }
    stages {
        stage('build') {
            steps {
                //sh 'mkdir /.m2'
                sh 'mkdir /.m2/repository'
                //checkout scm
                //git url: 'git://github.com/zhxdong95/simple-web.git', branch: 'main'
                //sh 'cd simple-web'
                //sh 'mvn --version'
                //git 'https://github.com/zhxdong95/simple-web.git'
                sh 'mvn -X clean package'
            }
        }
    }
}
