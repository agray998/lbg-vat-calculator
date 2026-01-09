pipeline {
    agent any
    
    stages {
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
