pipeline {
    agent any
    tools {
        maven 'maven'   // make sure "maven" is the name you configured in Jenkins Global Tool Configuration
        jdk 'jdk'
    }
    stages {
        stage('Checkout From Git') { 
            steps {
                git branch: 'main', url: 'https://github.com/BakshiShubhali/springboot-jenkins-pipeline.git'
            }
        }
        stage('Maven Compile') {
            steps {
                echo "This is Maven Compile Stage"
                sh 'mvn clean compile'
            }
        }
    }
}