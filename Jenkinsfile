pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/Na4in2012/blueOceanDemo.git', branch: 'main')
      }
    }

    stage('build') {
      steps {
        echo 'This is build'
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deployto_Dev1') {
          steps {
            sleep 30
            echo 'Finish'
          }
        }

        stage('Deployto_Dev2') {
          steps {
            sleep 50
            echo 'Comleted'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'testing'
      }
    }

  }
}