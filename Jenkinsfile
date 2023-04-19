pipeline {
    agent any
    stages {
        stage('Checking python version') {
            steps {
                bat 'python -V'
            }
        }
        stage('Cloning repository') {
            steps {
                bat 'xcopy C:\\Users\\HP\\.jenkins\\workspace\\abhishek\\* E:\\devops\\htdocs\\exp4\\ /Y /S'
            }
        }
        stage('Deploying HTML files') {
            steps {
                bat 'xcopy *.html E:\\devops\\htdocs\\exp4\\ /Y /S'
            }
        }
        stage('Printing done') {
            steps {
                echo 'Done'
            }
        }
    }
}



