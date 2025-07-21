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
        }
        stage('cloning repo') {
            steps {
              ansiblePlaybook credentialsId: 'ansible', installation: 'ansible', inventory: 
              '/webapp/roles-03/hosts.ini', playbook: '/webapp/roles-03/03-role-playbook.yml'
            }
        }
    }
}