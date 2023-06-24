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
    
}}
