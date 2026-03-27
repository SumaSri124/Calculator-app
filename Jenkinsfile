pipeline {
agent any

```
stages {
    stage('Checkout Code') {
        steps {
            git 'https://github.com/SumaSri124/calculator-app.git'
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

    stage('Install to Local Repo') {
        steps {
            sh 'mvn install'
        }
    }
}

post {
    success {
        archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
    }
    failure {
        echo 'Build failed'
    }
}
```

}
