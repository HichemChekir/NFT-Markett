pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'npm --version'
            }
        }
        stage('Test') {
            steps {
                sh 'npx hardhat test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'npx hardhat run scripts/deploy.js --network ropsten'
            }
        }
    }
} 