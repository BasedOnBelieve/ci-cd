pipeline {
    agent {label 'ansible'}
    
    stages {
        
        stage('verify git') {
            steps {
                sh 'which git'
                sh 'git --version'
            }
        }
        stage('git checkout') {
            steps {
                    checkout scm
            }  
        }/*
        stage('cloning repo') {
            steps {
              git  url: 'https://github.com/BasedOnBelieve/ci-cd.git', branch: 'main'
            }
        }*/
    }
}