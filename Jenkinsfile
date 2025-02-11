pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                echo 'Compiling the Java program...'
                bat 'javac TimestampPrinter.java'
            }
        }

        stage('Run') {
            steps {
                echo 'Running the program to print timestamp...'
                bat 'java TimestampPrinter'
            }
        }
    }

    post {
        always {
            echo 'Build complete!'
        }
    }
}
