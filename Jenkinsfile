pipeline {
  agent any
  stages {
    stage('install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('fetch code') {
      steps {
        git(url: 'https://github.com/premjithbenny/blueocean.git', branch: 'main')
      }
    }

    stage('deployee') {
      steps {
        sh 'sudo cp -R . /var/www/html/'
      }
    }

  }
}