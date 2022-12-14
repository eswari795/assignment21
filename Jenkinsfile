pipeline{
    
    agent any
    
    stages{
        
        stage("chckout git repo"){
            steps{
                git 'https://github.com/eswari795/assignment21.git'
            }
        }
        
        stage("deploy using ansible"){
            steps{
                ansiblePlaybook credentialsId: 'Ansible', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'dev.inv', playbook: 'apache.yml'
            }
        }
    }
}
