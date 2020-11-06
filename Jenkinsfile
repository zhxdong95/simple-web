pipeline {
    agent { docker 'maven:3.6.3' }
    stages {
        stage('build') {
            steps {
                checkout scm
                //sh 'cd simple-web'
                sh 'mvn --version'
                //git 'https://github.com/zhxdong95/simple-web.git'
                sh 'mvn clean package'
            }
        }
    }
}