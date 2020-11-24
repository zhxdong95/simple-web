pipeline {
    agent {
        docker {
            image 'maven:3.6.3-ibmjava-alpine'
            args '-u root -v $HOME/.m2:/root/.m2 -v /home/data/mvnRepository:/root/.m2/repository'
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
