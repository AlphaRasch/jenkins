pipeline {
    agent {
        docker {
            image 'g++:latest' // Замените на имя образа, соответствующего вашему компилируемому языку программирования
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o main main.o main.cpp' // Замените на соответствующую команду сборки вашего проекта
            }
        }
    }
    post {
        success {
            archiveArtifacts artifacts: 'main.o' // Замените на соответствующий путь/имя готового бинарника
        }
    }
}
