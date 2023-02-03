pipeline {
    agent {
      label 'ansible'
    }
    stages {
        stage('first') {
            steps {
                sh 'ansible-galaxy install -r requirements.yml -p . '
                sh 'cd vector'
                sh 'molecule test -s podman'
            }
        }
    }
}