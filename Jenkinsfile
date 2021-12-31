pipeline {
  agent any

  stages {
    stage('Hello') {
      steps {
        sh '''
          ansible --version
          ansible -m ping hq_devices
        '''
      }
    }
  }
}
