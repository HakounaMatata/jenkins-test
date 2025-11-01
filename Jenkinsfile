@Library('jenkins-shared-lib') _

pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo "📦 Cloning repository..."
                git branch: 'main', url: 'https://github.com/Hassan-Eid-Hassan/python-iti.git'
            }
        }

        stage('Greeting') {
            steps {
                script {
                    greet('Abdelrahman')
                }
            }
        }

        stage('Build App') {
            steps {
                script {
                    buildApp()
                }
            }
        }

        stage('Docker Ops') {
            steps {
                script {
                    dockerOps.buildAndPush('abdelkaderjr/python-iti-java', '1.0')
                }
            }
        }
    }
}
