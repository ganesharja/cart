@Library ("roboshop-shared-library@main") 

pipeline {
    agent any 
    stages {
        stage('Lint Checks') {
            steps {
                script {
                    sample.info()
                } 
                sh "echo Installing JSlist"
                sh "npm i jslint"
                sh "echo starting lintchecks"
                sh "node_modules/jslint/bin/jslint.js server.js || true"
                sh "echo lintChecks completed"
            }
        }
        stage('Generating Artifacts') {
            steps {
                sh "echo Generating Artifacts..."
                sh "npm install" 
            }
        }
    }
} 