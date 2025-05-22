pipeline{
    agent any

    stages{
        stage('Checkout'){
            steps {
                echo 'Checking out Source Code'
                checkout scm
            }
        }

        stage('Installing Dependencies'){
            steps{
                echo 'Installing Python Dependencies'
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests'){
            steps{
                echo 'Running tests using pytest'
                bat 'pytest'
            }
        }
    }

    post{
        success{
            echo 'Pipeline Succeeded!!'
        }

        failure{
            echo 'Pipeline failed!'
        }
    }
}