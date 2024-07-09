pipeline {
    agent {
        label 'linux'
    }
    stages {
        stage('First'){
            steps {
                sh 'git clone https://github.com/reocoker85/nginx-role.git'
                sh 'cd nginx-role'
            }
        }
        stage('Second'){
            steps {
                sh 'molecule init scenario --driver-name docker'
                sh 'molecule test'
            }
        }
    }
}
