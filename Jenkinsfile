pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is the build job'
        sh 'npm install'
      }
    }
pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs' 
    }
    

    stages{
        stage('Build'){
            steps{
                echo 'this is the build job'
                sh 'npm install'

                          }
        }
        stage('two'){
            steps{
                echo 'this is the Test job'
                sh 'npm test'
                
            }
        }
        stage('three'){
            steps{
                echo 'this is the Package Job'
                sh 'npm run package'
                
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
    stage('test') {
      steps {
        echo 'this is the test job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
      }
    }

    stage('artifact') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}
