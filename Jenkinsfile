pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                
            }
        }
        stage('Test') {
            steps {
                sh 'npx hardhat test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'npx hardhat run ./scripts/deploy.js --network ropsten'
            }
        }
    }
} 