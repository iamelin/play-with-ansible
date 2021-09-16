#!groovy

pipeline {
    stages {
        stage('Deploy') {
            steps {
                script {
                    echo '### Deploy ###'
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
