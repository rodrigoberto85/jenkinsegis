pipeline {
  agent any
  stages {
    stage('run_pdi') {
      steps {
        sh '/opt/pdi-ce-5.2.0.0-209/data-integration/pan.sh -file=/opt/unidadeNegocio/UN_AUTOMATICA.ktr'
      }
    }
    stage('Fim') {
      steps {
        git(changelog: true, poll: true, url: 'https://github.com/rodrigoberto85/jenkinsegis', branch: 'unidadenegocio', credentialsId: '610d5a14bcad078df17f575589a6e0e006fd44ba')
      }
    }
  }
  environment {
    unidadenegocio = 'unidadenegocio'
  }
}