pipeline {
    agent any

    stages {
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