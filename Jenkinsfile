pipeline {
    agent {
        docker {
            image 'g++:latest' 
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o main main.o main.cpp' 
            }
        }
    }
    post {
        success {
            archiveArtifacts artifacts: 'main.o' 
        }
    }
}
