pipeline {
    agent any
    stages {
        stage('Deploy Nginx') {
            steps {
                echo 'Deploying NGINX'
                ansiblePlaybook(
                    playbook: 'nginx/nginx_install.yaml',
                    credentialsId: 'ansible_sshkey'
                )
            }
        }
        stage('Install Parts') {
            steps {
                echo 'Installing parts to VM'
                ansiblePlaybook(
                    playbook: 'vm-docker/installingparts.yaml',
                    credentialsId: 'ansible_sshkey'
                )
            }
        }
        stage('Deploy Docker') {
            steps {
                echo 'Deploying Docker'
                ansiblePlaybook(
                    playbook: 'vm-docker/installdocker.yaml',
                    credentialsId: 'ansible_sshkey'
                )
            }
        }
        stage('Deploy Container Services') {
            steps {
                echo 'Deploying all services to Docker container'
                ansiblePlaybook(
                    playbook: 'vm-docker/containerservices.yaml',
                    credentialsId: 'ansible_sshkey'
                )
            }
        }
    }
}