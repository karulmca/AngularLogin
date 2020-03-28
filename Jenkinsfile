pipeline{
  agent { label 'nodejs8' }
  stages{
    stage ('checkout'){
      steps{
        checkout scm
        git branch: 'master', url: 'git@github.com:karulmca/AngularLogin.git'
      }
    }
   }
   
    
  }

