pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Windows command
                // bat 'git clone https://github.com/raviaare/springexample.git'
                // Linux command
                sh "rm -rf springexample"
                sh 'git clone https://github.com/raviaare/springexample.git'
                sh "mvn clean -f springexample"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test -f springexample"
            }
        }
        stage('Deploy') {
            steps {
                sh "mvn package -f springexample"
            }
        }
    }
}
