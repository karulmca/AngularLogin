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
    stage ('install modules'){
      steps{
        sh '''
          npm install --verbose -d 
          npm install --save classlist.js
        '''
      }
    }
  
    
    stage ('build') {
      steps{
        sh '$(npm bin)/ng build --prod --build-optimizer'
      }
    }
    stage ('build image') {
      steps{
        sh '''
          rm -rf node_modules
          oc start-build angular-5-example --from-dir=. --follow
        '''
      }
    }
  }

