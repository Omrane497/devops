
pipeline {
    agent {
        label 'ansible-agent'
    }

    stages {
        stage('Checkout DevOps Repository') {
            steps {
                checkout scm
            }
        }

        stage('Deploy Flask Application') {
            steps {
                sh 'JENKINS_NODE_COOKIE=dontKillMe ansible-playbook -i inventory.ini deploy.yml'
            }
        }
    }
}
