pipeline {
    agent any
    tools {
        maven 'maven'   // make sure "maven" is the name you configured in Jenkins Global Tool Configuration
    }
    stages {
        stage('Checkout From Git') { 
            steps {
                git branch: 'main', url: 'https://github.com/BakshiShubhali/springboot-jenkins-pipeline.git'
            }
        }
        stage('Maven Validate') {
            steps {
                echo "This is Maven Validate Stage"
                sh 'mvn validate'
            }
        }
        stage('Maven Compile') {
            steps {
                echo "This is Maven Compile Stage"
                sh 'mvn compile'
            }
        }
        stage('Maven Package') {
            steps {
                echo "This is Maven Package Stage"
                sh 'mvn package'
            }
        }
    }
}