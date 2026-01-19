pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub'
            }
        }

        stage('Infrastructure Deployment') {
            steps {
                echo 'Running Ansible playbook via Jenkins'
                echo 'ansible-playbook -i ansible/inventory.ini ansible/playbook.yml'
            }
        }
    }

    post {
        success {
            echo 'Infrastructure change executed via Jenkins'
        }
        failure {
            echo 'Infrastructure change failed'
        }
    }
}
