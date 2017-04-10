pipeline {
  agent any
  stages {
    stage('run_pdi') {
      steps {
        sh '/opt/pdi-ce-5.2.0.0-209/data-integration/pan.sh -file=/opt/unidadeNegocio/UN_AUTOMATICA.ktr'
      }
    }
  }
  environment {
    unidadenegocio = 'unidadenegocio'
  }
}