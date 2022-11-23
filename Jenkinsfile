pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       nodejs 'nodejs' 
    }    

    stages{
        stage('build-the-app-stage'){
            steps{
                echo 'this is the first job to build'
                sh 'npm install'
            }
        }
        stage('test-the-app-stage'){
            steps{
                echo 'this is the second job to test'
                sh 'npm test'
            }
        }
        stage('package-the-app-stage'){
            steps{
                echo 'this is the third job to package'
                sh 'npm run package'
            }
        }
    }
    
    post{
        always{
            echo 'this 3 stage pipeline has completed...'
        }
        
    }
    
}