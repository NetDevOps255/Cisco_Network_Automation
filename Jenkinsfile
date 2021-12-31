pipeline {
  agent any

  stages {
    stage('Clone Repository') {
      steps {
        git clone https://github.com/NetDevOps255/Cisco_Network_Automation.git
      }
    }
    stage('Test Device Reachability') {
      steps {
        sh '''
          /* ansible-galaxy collection install -r requirements.yml
          ansible -m ping hq_devices
        '''
      }
    }
  }
}
