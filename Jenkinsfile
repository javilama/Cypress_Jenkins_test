pipeline {
    agent any
    
    stages {
        stage("Clonar repositorio") {
            steps {
                //git 'https://github.com/javilama/TestCypressTS.git'
                sh 'npm install'

            }
            steps{
                sh 'cypress install' 
            }
        }
        
        stage("run tests") {
            steps {
                sh 'npx cypress run --spec cypress/e2e/testpage.cy.js'
            }
        }
    }
}