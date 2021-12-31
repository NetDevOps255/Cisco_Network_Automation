pipeline {
  agent any

  stages {
    stage('Test Device Reachability') {
      steps {
        sh '''
          /* ansible-galaxy collection install -r requirements.yml
          ansible -m ping hq_devices
        '''
      }
    }
    
    stage('Running Ansible Playbook') {
      steps {
        sh 'ansible-playbook config-backup.yml'
      }
    }
  }
}
