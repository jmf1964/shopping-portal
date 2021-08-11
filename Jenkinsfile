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
        stage('Test'){
            steps{
                echo 'this is the npm test'
                sh 'uptime'
                 }
        }
        stage('Package'){
            steps{
                echo 'this is the Package job'
                sh 'npm test'
                
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
