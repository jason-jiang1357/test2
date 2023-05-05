pipeline {
  agent any
  stages {
    stage('stage 1') {
      environment {
        name = 'jwf'
      }
      parallel {
        stage('stage 1') {
          steps {
            sh 'echo "step 1"'
            sh 'echo "step 2"'
            echo 'step3 print message'
            git(url: 'git@github.com:jiangwenfan/test.git', branch: 'main')
            sleep 2
          }
        }

        stage('two') {
          steps {
            sh 'echo "222"'
            echo 'hello'
          }
        }

      }
    }

    stage('stage 2') {
      steps {
        sh 'echo "step 1"'
      }
    }

  }
  environment {
    age = '888'
  }
}