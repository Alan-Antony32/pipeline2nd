pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                echo 'Pulling code from Git repository'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building website (static build)'
                sh 'ls -l'
            }
        }

        stage('Test Website Files') {
            steps {
                echo 'Running validation tests'
                sh 'bash test.sh'
            }
        }

        stage('Final Output') {
            steps {
                echo 'CI Pipeline executed successfully'
                sh 'echo "Website pipeline completed successfully"'
            }
        }
    }

    post {
        success {
            echo '✅ PIPELINE SUCCESS'
        }
        failure {
            echo '❌ PIPELINE FAILED'
        }
    }
}
