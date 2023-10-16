pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Check out your Git repository
                script {
                    def scmVars = checkout scm
                }
            }
        }

        stage('Build') {
            steps {
                // Compile the Java code
                sh 'javac HelloWorld.java'
            }
        }

        stage('Run') {
            steps {
                // Run the Java program
                sh 'java HelloWorld'
            }
        }
    }

    post {
        success {
            echo 'Build and execution successful!'
        }
    }
}
