pipeline {
    agent {
        any {
            image 'gcc:latest' 
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o binary_search main.cpp' 
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts 'binary_search' 
            }
        }
    }
}
