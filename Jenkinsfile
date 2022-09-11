pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
               checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'mahi49', url: 'https://github.com/mahi49/JENKINS-PIPELINE.git']]])}
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage ('validate') {
            steps {
                sh 'mvn validate'
            }

        }
        stage ('test') {
            steps {
                sh 'mvn test'
            }
        }
         stage ('package') {
            steps {
                sh 'mvn package'
        
            }

         }    


    }
} 
