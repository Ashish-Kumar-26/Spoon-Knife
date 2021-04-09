pipeline {
  agent any
  stages {
    stage('Log Tool version') {
      parallel {
        stage('Log Tool version') {
          steps {
            sh '''git --version
java --version
docker --version'''
          }
        }

        stage('check for index') {
          steps {
            fileExists 'index.html'
          }
        }

      }
    }

    stage('post build steps') {
      steps {
        writeFile(file: 'status.txt', text: 'hey it worked..!!!')
      }
    }

  }
}