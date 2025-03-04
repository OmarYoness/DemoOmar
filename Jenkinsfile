pipeline {
    agent any

    tools {
        maven 'Maven' // Use the name you set in Jenkins for Maven
    }

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/OmarYoness/DemoOmar.git'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
}

