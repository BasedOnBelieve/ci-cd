pipeline {
    agent any
    
    stages {
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