pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'building my application'
          }
        }

        stage('test') {
          steps {
            echo 'i have tested my solution'
            echo 'im here'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        archiveArtifacts(allowEmptyArchive: true, onlyIfSuccessful: true, artifacts: '**')
      }
    }

  }
  environment {
    chromDriverpath = '${ChromeDriverPath}'
  }
}