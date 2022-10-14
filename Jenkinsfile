pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'this is my first step'
          }
        }

        stage('build2') {
          steps {
            sh 'pwd'
          }
        }

      }
    }

    stage('CQ') {
      steps {
        sh '''pwd
ls
date'''
      }
    }

    stage('deploy_SIT') {
      steps {
        sleep 10
      }
    }

    stage('deploy_to_UAT') {
      steps {
        echo 'this is my final stage'
      }
    }

  }
}