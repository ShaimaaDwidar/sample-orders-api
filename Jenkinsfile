pipeline {
  agent any
  
  tools {
    nodejs 'node'
  }

  environment {
    APIC_SERVER = 'https://apic.example.com'
    APIC_ORG    = 'my-org'
    APIC_CATALOG= 'dev'
  }

  stages {

    stage('Validate OpenAPI') {
      steps {
        sh 'apic drafts:validate api/orders_api.yaml'
      }
    }
  }
}
