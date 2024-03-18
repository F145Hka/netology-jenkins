pipeline {
    agent {
        label 'docker'
    }
    stages {
        stage('Delete prev') {
            steps {
                deleteDir()
            }
        }
        stage('Clone repo') {
            steps {
                git branch: 'master', url: 'https://github.com/F145Hka/ansible-vector-role.git'
            }
        }
        stage('Run molecule test') {
            steps {
                sh 'molecule test'
            }
        }
    }
}
