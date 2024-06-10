pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/raghuldesai/Ekart.git'
            }
        }
        stage("Build") {
            steps {
                sh "mvn clean install -DskipTests=true"
            }
        }
    }
}
