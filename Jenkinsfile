pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Ahsan-Asim/network_automation.git'
            }
        }
        stage('Deploy Configurations') {
            steps {
                bat 'wsl ansible-playbook -i ansible/inventory.ini ansible/playbook.yml'
            }
        }
    }
}
