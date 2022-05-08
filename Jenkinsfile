pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                npm --version
            }
        }
        stage('Test') {
            steps {
                npx hardhat test
            }
        }
        stage('Deploy') {
            steps {
                npx hardhat run scripts/deploy.js --network ropsten
            }
        }
    }
} 