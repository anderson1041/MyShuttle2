pipeline {
    agent any
    environment {
        BRANCH = 'Master'
    }
    stages {
        stage('Build') {
            environment{
                VARIAVEL = 'variavel'
            }
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
