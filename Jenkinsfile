pipeline {
    agent any
    
    stages {
        
        stage('Building') {
            steps {
                echo 'The code will be now build into an artifact'
            }
        }
        stage('Artifact Archiving') {
            steps {
                echo 'The Artifact will be uploaded to an artifact repository'
            }
        }
        stage('Testing') {
            steps {
                echo 'The Artifact will be tested'
            }
        }
        stage('Staging') {
            steps {
                echo 'The Artifact is staged onto the staging server'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Artifact is been deployed'
            }
        }
    }
    post{
        always{
            emailext body: 'Summary', subject: 'Pipeline Status', to: 'sakshi.shelke29@gmail.com'
        }
    }
}
