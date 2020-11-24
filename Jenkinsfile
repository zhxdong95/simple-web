pipeline {
    agent {
        docker {
            image 'maven:3.6.3'
            args '-v $HOME/.m2:${user.home}/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo Building ...'
                //sh 'mkdir /.m2'
                //sh 'sudo mkdir /.m2/repository'
                //checkout scm
                //git url: 'git://github.com/zhxdong95/simple-web.git', branch: 'main'
                //sh 'cd simple-web'
                //sh 'mvn --version'
                //git 'https://github.com/zhxdong95/simple-web.git'
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'echo Testing ...'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Deploying ...'
            }
        }
    }
}
