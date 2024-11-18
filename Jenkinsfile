pipeline {
    agent any

    stages {
        stage("Package") {
            steps {
                echo "Packaging the application..."
                sh "./gradlew build"
            }
        }

        stage("Docker Build") {
            steps {
                echo "Building Docker image..."
                sh "docker build -t localhost:5000/calculatrice ."
            }
        }
    }
}

