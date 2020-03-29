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
      steps{
                sh "npm install"
        }
    }
        stage('Build'){
          steps{
                sh "npm run build:ssr"
        }
        }
        stage('Deploy'){
          steps{
                sh "pm2 restart all"
          }
        }
   }
   
    
  }

