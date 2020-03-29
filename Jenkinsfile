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
                sh "pm2 start server/index.js"
                sh "npm install"
                //sh "npm install pm2 -g"
        }
    }
        stage('Build'){
          steps{
                sh "npm run build"
        }
        }
        stage('Deploy'){
          steps{
                //sh "pm2 startOrGracefulReload current/ecosystem.config.js --update-env"
                sh "pm2 restart all"
          }
        }
   }
   
    
  }

