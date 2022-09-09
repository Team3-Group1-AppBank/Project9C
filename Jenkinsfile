pipeline{
  agent any
  stages{
    stage('git-clone'){
     steps{
        checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'team3hook', url: 'https://github.com/Team3-Group1-AppBank/Project9C.git']]])
     

     }
    }
        stage('Feature Branch Deploy Code') {
            when {
                branch 'feature'
            }
            steps {
                sh 'echo "Building Artifact from Feature branch"'
                sh 'echo "Deploying Code from Feature branch"'
           }
        }
        stage('Develop Branch Deploy Code') {
           when {
                branch 'develop'
            }
            steps {
                sh 'echo "Building Artifact from Develop branch"'
                sh 'echo "Deploying Code from Develop branch"'
           }
        }
        
      stage('Main Branch Deploy Code') {
            when {
                branch 'main'
            }
            steps {
                sh 'echo "Building Artifact from Main branch"'
                sh 'echo "Deploying Code from Main branch"'
            }
        }

    }

}
