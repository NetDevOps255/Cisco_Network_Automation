pipeline {
  agent any

  stages {
    stage('Clone Repository') {
      steps {
        git credentialsId: 'c0da821f-39f7-4f6f-a661-d1aba0940c89', url: 'https://github.com/NetDevOps255/Cisco_Network_Automation.git'
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
