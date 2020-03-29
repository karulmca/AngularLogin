pipeline{
  agent any
  tools {nodejs "Node"}
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
         sh 'npm run build'
      }
    } 
    stage('Test') {
      steps {
         sh 'npm test'
      }
    } 
   }
   
    
  }

