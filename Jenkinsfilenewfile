pipeline {
    agent any
    tools {
        maven 'maven'   // make sure "maven" is the name you configured in Jenkins Global Tool Configuration
    }
    stages {
        stage('Checkout From Git') { 
            steps {
                git branch: 'prod', url: 'https://github.com/BakshiShubhali/springboot-jenkins-pipeline.git'
            }
        }
        stage('Maven Compile') {
            steps {
                echo "This is Maven Compile Stage"
                bat 'mvn clean compile'
            }
        }
        stage('Maven Test') {
            steps {
                echo "This is Maven Test Stage"
                bat 'mvn test'
            }
        }
        stage('Maven Package') {
            steps {
                echo "This is Maven Package Stage"
                bat 'mvn package'
            }
        }
    }
}