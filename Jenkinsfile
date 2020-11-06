pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                //checkout scm
                git url: 'git://github.com/zhxdong95/simple-web.git', branch: 'main'
                //sh 'cd simple-web'
                sh 'mvn clean package'
            }
        }
    }
}