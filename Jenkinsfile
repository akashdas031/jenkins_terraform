pipeline {
  agent any
     environment {
       AWS_ACCESS_KEY = credentials('AWS_ACCESS_KEY')
       AWS_SECRET_ACCESS_KEY= credentials('AWS_SECRET_ACCESS_KEY')
     }
  stages {
    stage ('checkout') {
      steps {
        checkout scm
      }
    }
    stage ('Terraform init') {
      steps {
        sh 'terraform init'
      }
    }
    stage ('Terraform plan') {
      steps {
        sh 'terraform plan'
      }
    }
    stage ('Terraform apply') {
      steps {
        sh 'terraform apply --auto-approve'
      }
    }
  }
}
    
