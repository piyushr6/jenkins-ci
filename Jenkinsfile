pipeline {
 agent any
 stages {
 stage('Clone') {
 steps {
 git branch: 'master', url: 'https://github.com/piyushr6/jenkins-ci.git'
 }
 }
 stage('Build') {
 steps {
 sh '''
 echo "Building Java project..."
 echo "Listing workspace contents: "
 ls
 mkdir -p build
 javac -d build src/*.java
 echo "Build successful"
 '''
 }
 }
 }
}
