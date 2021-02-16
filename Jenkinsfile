pipeline {
  agent any
  stages {
    stage('HolaMundo') {
      steps {
        echo 'holamundo'
        writeFile(file: 'archivo.txt', text: 'hola mundo')
      }
    }

    stage('Guardar') {
      steps {
        archiveArtifacts '*.txt'
      }
    }

  }
}