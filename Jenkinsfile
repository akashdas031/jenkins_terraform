pipeline {
  agent any
     enviroment {
       AWS_ACCESS_KEY_ID = credentials('AWS_ACCESS_KEY_ID')
       AWS_SECRET_KEY_ID = credentials('AWS_SECRET_KEY_ID')
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
    
