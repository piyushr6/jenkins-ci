pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/DecayDestructor/jenkins-ci-demo.git'
            }
        }
        stage('Build') {
            steps {
                sh '''
                echo "Building Java project..."
                mkdir -p build
                javac -d build src/*.java
                echo "Build successful"
                '''
            }
        }
    }
}
