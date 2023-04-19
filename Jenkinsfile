pipeline {
    agent any
    stages {
        stage('Checking python version') {
            steps {
                bat 'python --version'
            }
        }
        stage('Cloning repository') {
            steps {
                bat 'git clone <repository URL> C:/Xamp/htdocs/devopsexpone'
            }
        }
        stage('Printing done') {
            steps {
                echo 'Done'
            }
        }
    }
}
