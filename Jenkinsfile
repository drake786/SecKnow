pipeline {
  agent {
    docker {
      image 'debian'
    }

  }
  stages {
    stage('Primerpaso') {
      parallel {
        stage('Primerpaso') {
          steps {
            echo 'Primer Paso'
            sleep 2
            echo 'Sigo aqui...'
            isUnix()
          }
        }
        stage('Alterno o Paralelo') {
          steps {
            git 'https://github.com/drake786/blocklist-ipsets.git'
          }
        }
      }
    }
    stage('Segundo Paso') {
      steps {
        input(message: 'Seguro?', id: '1', ok: '1')
      }
    }
  }
}