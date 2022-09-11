pipeline{
  agent any
  stages{
    
    stage('git-clone'){
    	steps{
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'team3hook', url: 'https://github.com/topsicle1/EnforcedMultibranch.git']]])
    	
    	}
    }
     stage('Feature Branch Deploy Code') {
            when {
                branch 'feature'
            }

      parallel{
        stage('actions1'){
          steps{
            sh 'pwd'
          }
        }
        stage('actions2'){
          steps{
            sh 'lscpu'
          }
        }
            stage('actions7'){
          steps{
            sh 'lscpu'
          }

        }
            stage('actions8'){
          steps{
            sh 'lscpu'
          }
        }
      }
    }
   
     
   stage('Develop Branch Deploy Code') {
            when {
                branch 'develop'
            }  
  
      parallel{
        stage('actions3'){
          steps{
            sh 'pwd'
          }

        }
        stage('actions4'){
          steps{
            sh 'lscpu'
          }
        }
                 stage('actions7'){
          steps{
            sh 'lscpu'
          }
        }
            stage('actions8'){

          steps{
            sh 'lscpu'
          }
        }
      }
    }
    
     stage('Main Branch Deploy Code') {
            when {
                branch 'main'
            }  
  
      parallel{
        stage('actions5'){
          steps{
            sh 'pwd'
          }
        }
        stage('actions6'){
          steps{
            sh 'lscpu'
          }
        }

                 stage('actions7'){
          steps{
            sh 'lscpu'
          }
        }
            stage('actions8'){
          steps{
            sh 'lscpu'
          }
        }

      }
    }
  }
}   
 
