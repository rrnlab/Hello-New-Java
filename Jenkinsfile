pipeline {

    agent any

    stages{

        stage('Git Checkout'){

            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/rrnlab/Hello-New-Java.git']]])
            }
        }
        stage('Maven Install'){

            steps{
                sh 'mvn compile'
            }
        }
        stage('Maven Unit Test'){

            steps{
                sh 'mvn test'
            }
        }
    }
}