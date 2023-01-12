pipeline {
  agent any
  stages {
    stage('Fetch Code') {
      steps {
        git(url: 'https://github.com/thangapandiyanp/html.git', branch: 'master', poll: true)
      }
    }

    stage('install apache') {
      steps {
        sh '''sudo apt install apache2 -y

'''
      }
    }

    stage('Deploy') {
      steps {
        sh 'sudo cp -R * /var/www/html'
      }
    }

  }
}