pipeline {
    agent none

    stages {

        stage('verify git') {
            agent {label 'ans'}
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

        /*
        stage('cloning repo') {
            steps {
                ansiblePlaybook(
                    credentialsId: 'ansible',
                    installation: 'ansible',
                    inventory: 'roles-03/hosts.ini',
                    playbook: 'roles-03/03-role-playbook.yml'
                )
            }
        }
        

        stage('run ansible manually') {
            steps {
                sh '''
                /usr/bin/ansible-playbook webapp/roles-03/03-role-playbook.yml \
                    -i roles-03/hosts.ini \
                    --private-key ssh12547533458778676982.key \
                    -u ec2-user
                '''
            }
        }*/
    }
}
