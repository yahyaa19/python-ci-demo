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
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests'){
            echo 'Running tests using pytest'
            sh 'pytest'
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