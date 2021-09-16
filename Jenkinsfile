#!groovy

pipeline {
    agent any

    stages {
        stage('Run Ansible') {
            steps {
                script {
                    echo '### Ansible ###'
                    ansiColor('xterm') {
                        ansiblePlaybook(
                            colorized: true,
                            forks: 5,
                            installation: 'ansible28',
                            playbook: 'my-playbook.yml',
                            vaultCredentialsId: 'VAULT_PASSWORD',
                            disableHostKeyChecking: true,
                            sudoUser: null
                        )
                    }
                }
            }
        }

    }
}
