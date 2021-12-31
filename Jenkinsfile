pipeline {
  agent any

  stages {
    stage('Clone Repository') {
      steps {
        checkout scm
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
