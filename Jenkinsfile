pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        build(job: 'name', propagate: true)
        sh 'echo "Ram"'
      }
    }

    stage('ansi') {
      steps {
        ansiblePlaybook(become: true, playbook: 'jenkins_yaml', becomeUser: 'root', colorized: true, forks: 2)
      }
    }

  }
}