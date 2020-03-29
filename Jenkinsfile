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
   //stage('Build') {
    //  steps {
//sh 'npm install'
   //   }
   // } 
    //stage('Test') {
      //steps {
      //   sh 'npm test'
      //}
   // } 
    
    stage('Install node modules'){
                sh "npm install"
        }
        stage('Build'){
                sh "npm run build:ssr"
        }
        stage('Deploy'){
                sh "pm2 restart all"
        }
   }
   
    
  }

