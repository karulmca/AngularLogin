pipeline{
  agent any
  tools {nodejs "node"}
  stages{
    stage ('checkout'){
      steps{
        checkout scm
        git branch: 'master', url: 'https://github.com/karulmca/AngularLogin.git'
      }
    }
    stage('Build') {
      steps {
        sh 'npm install'
         sh '<<Build Command>>'
      }
    }  
   }
   
    
  }

