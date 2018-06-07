#!groovy

pipeline {
    agent { label 'ubuntu16' }

    stages {
        stage('Shellcheck') {
            steps {
                shellcheck()
            }
        }
        stage('Ansible Syntax Check') {
            steps {
                ansibleCheckSyntax((String[])["playbook.yml"], "inventory")
            }
        }
    }
}
