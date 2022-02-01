pipeline {
    agent any

    stages {
        stage('continous download') {
            steps {
                git 'https://github.com/77vijju/DemoATC.git'
            }
        }
        stage('mvn build') {
            steps {
                sh 'mvn install'
            }
        }
        stage('continues deployment') {
            steps {
                sh 'sshpass -p "vijju" scp target/DemoATC.war vijju@172.17.0.2:/opt/apache-tomcat-9.0.56/webapps'
            }
        }
    }
}
