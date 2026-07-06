PetClinic DevOps

Architecture

GitHub (Application)
        │
        
Azure DevOps Pipeline
        │
        
Build (Maven)
        │
        
Publish Artifact
        │
        
Ansible Deployment
        │
        
Azure VM
        │
        
Spring Boot
        │
        
Prometheus
        │
        
Grafana


for local ansible trigger: 

ansible-playbook \
-i ansible/inventories/dev/hosts.ini \
ansible/playbooks/deploy.yml \
--private-key ~/.ssh/petclinic-key.pem \
-e "artifact_path=$(pwd)/artifacts/spring-petclinic.jar"

ansible-playbook -i ansible/inventories/dev/hosts.ini ansible/playbooks/bootstrap.yml --private-key ~/.ssh/petclinic-key.pem


connect to vm
 ssh -i ~/.ssh/petclinic-key.pem azureuser@4.223.161.140