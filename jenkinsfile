pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                npm install
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