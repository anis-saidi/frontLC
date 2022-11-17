pipeline
{
   agent any
    stages {
     
      
       
     stage ('build'){
      steps{
        script{
            sh  "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml -e ansible_become_password=123456"
        }  
      }
     
     }
     stage('docker'){
            steps{
                script{
                    sh "ansible-playbook Ansible/docker.yml -i Ansible/inventory/host.yml -e ansible_become_password=123456"
                }
            }
        }
        stage('docker-registry'){
            steps{
                script{
                    sh "ansible-playbook Ansible/docker-registry.yml -i Ansible/inventory/host.yml -e ansible_become_password=123456"
                }
            }
        } 
         }
         }
