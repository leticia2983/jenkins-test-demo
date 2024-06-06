pipeline {
    agent any

    stages {
        stage('checkout') {
            steps {
               checkout scmGit(branches: [[name: 'main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/leticia2983/pytest-intro-vs.git']])
            }
        }
        stage('Build') {
            steps {
               git branch: 'main', url: 'https://github.com/leticia2983/pytest-intro-vs.git'
               sh 'python3 ops.py'
            }
        }
        stage('Test') {
            steps {

               sh 'python3 -m pytest'
            }
        }
    }

}