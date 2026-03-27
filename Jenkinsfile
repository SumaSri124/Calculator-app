pipeline {
agent any

stages {
    stage('Checkout Code') {
        steps {
            git branch: 'main', url: 'https://github.com/SumaSri124/Calculator-app'
        }
    }

    stage('Build & Test') {
        steps {
            sh 'mvn clean test'
        }
    }

    stage('Package JAR') {
        steps {
            sh 'mvn package'
        }
    }
}

}
