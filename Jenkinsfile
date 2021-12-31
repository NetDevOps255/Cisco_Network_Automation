pipeline {
  agent any

  stages {
    stage('Hello') {
      steps {
        sh '''
          ansible-galaxy collection install -r requirements.yml
          ansible -m ping hq_devices
        '''
      }
    }
  }
}
