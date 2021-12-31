pipeline {
  agent any

  stages {
    stage('Test Device Reachability') {
      steps {
        sh '''
          ansible-galaxy collection install -r requirements.yml
          ansible -m ping hq_devices
        '''
      }
    }
    
    stage('Running Ansible Playbook') {
      steps {
        sh 'chmod 777 /home/travis/Network_Automation/GIT-Repo/Cisco_Network_Automation'
        sh 'ansible-playbook config-backup.yml'
      }
    }
  }
}
