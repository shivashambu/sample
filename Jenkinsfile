pipeline {
  agent any
  stages {
    stage('Fetch code') {
      steps {
        git(url: 'https://github.com/shivashambu/sample.git', poll: true)
      }
    }

    stage('install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('deploy app') {
      steps {
        sh 'sudo cp -R */var/www/html'
      }
    }

  }
}