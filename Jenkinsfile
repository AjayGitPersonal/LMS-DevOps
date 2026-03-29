pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/AjayGitPersonal/LMS-DevOps.git'
            }
        }

        stage('Frontend Build') {
            steps {
                dir('frontend') {
                    bat 'npm install'
                    bat 'npm run build'
                }
            }
        }

        stage('Backend Setup') {
            steps {
                dir('backend') {
                    bat 'npm install'
                }
            }
        }

        stage('Run Backend') {
            steps {
                dir('backend') {
                    bat 'npm start'
                }
            }
        }
    }
}
