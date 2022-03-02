pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'build'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'testing'
            sh '''mvn clean install
'''
          }
        }

        stage('UAT') {
          steps {
            echo 'uat'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploying'
      }
    }

  }
}