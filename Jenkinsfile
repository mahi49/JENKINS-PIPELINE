pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'mahi49', url: 'https://github.com/mahi49/JENKINS-PIPELINE.git']]])}
        }
        stage('validate') {
            steps {
                sh 'mvn validate'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }

        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
         stage('install') {
            steps {
                sh 'mvn install'
        
            }

         }    


    }
} 
