node {
    def app

    stage('Clone repository') {
        /* Cloning the Repository to our Workspace */

        checkout scm
    }
    */
   
    stage('Run Ansible Playbook') {
        /* This runs playbook */

         app = ansiblePlaybook credentialsId: '192.168.3.108', disableHostKeyChecking: true, inventory: 'hq_devices.inv', playbook: 'config-backup.yml'
    }
}
