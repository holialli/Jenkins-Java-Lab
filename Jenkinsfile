pipeline {
    agent any
    parameters {
        booleanParam(name: 'EXECUTE_TESTS', defaultValue: true, description: 'Check to run the Test stage')
    }
    stages {
        stage('Build') {
            steps {
                echo "Building Ali Ahmad's Project..."
                bat 'javac HelloWorld.java'
            }
        }
        stage('Test') {
            when {
                expression { params.EXECUTE_TESTS == true }
            }
            steps {
                echo 'Parameter was TRUE, running tests...'
                bat 'java HelloWorld'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
