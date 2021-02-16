pipeline {
  agent any
  stages {
    stage('HolaMundo') {
      steps {
        echo 'holamundo'
        writeFile(file: 'archivo.txt', text: 'hola mundo')
        bat 'echo %JENKINS_HOLA%'
        bat 'echo %PATH%'
      }
    }

    stage('Guardar') {
      steps {
        archiveArtifacts '*.txt'
      }
    }

    stage('Despedida') {
      steps {
        input(message: 'Lastima que termino', ok: 'Excelente taller')
      }
    }

  }
  environment {
    JENKINS_HOLA = 'josealbertolopez2'
  }
}