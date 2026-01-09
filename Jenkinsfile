pipeline {
    agent any
    
    stages {
        stage("Checkout Code") {
            steps {
                git url: "https://github.com/agray998/lbg-vat-calculator", branch: "main"
            }
        }
        stage("Install Deps") {
            steps {
                sh "npm install"
            }
        }
        stage("Run Tests") {
            steps {
                sh "CI=true npm test"
            }
        }
        stage("Build Webpack") {
            steps {
                sh "npm run build"
            }
        }
    }
}
