pipeline {
  agent any
  stages {
    stage('HolaMundo') {
      steps {
        echo 'holamundo'
        writeFile(file: 'archivo.txt', text: 'hola mundo')
        bat 'echo %JENKINS_HOLA%'
      }
    }

    stage('Guardar') {
      steps {
        archiveArtifacts '*.txt'
      }
    }

  }
  environment {
    JENKINS_HOLA = 'josealbertolopez2'
  }
}