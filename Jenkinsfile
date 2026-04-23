pipeline {
    agent any
    environment {
        STUDENT_NAME = "Ali Ahmad"
        ROLL_NO = "i232050"
    }
    stages {
        stage('Build') {
            steps {
                echo "Building for ${env.STUDENT_NAME}..."
                bat 'javac HelloWorld.java' 
            }
        }
        stage('Test') {
            steps {
                echo 'Running Tests...'
                bat 'java HelloWorld'
            }
        }
        stage('Deploy') {
    when {
        branch 'main'
    }
    steps {
        echo 'Deploying because we are on the main branch...'
    }
}
        stage('Deploy') {
            steps {
                echo 'Deploying to Production...'
                echo 'Artifacts secured.'
            }
        }
    }
    post {
        always {
            echo 'Lab 12 Pipeline execution finished.'
        }
    }
}
