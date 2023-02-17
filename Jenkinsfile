pipeline {
 agent any
 stages {
    stage('Build'){
        steps{
            sh 'make -C main'
            echo '🤞 Build stage successful'
        }
    }
    stage('Test'){
        steps{
            sh '/var/jenkins_home/workspace/PES1UG20CS537/main/hello_exec'
            echo '✅Testing completed' 
        }
    }
    stage('Deploy'){
        steps{
            echo 'Deploying..'
            echo '✅ Deployment successful'
        }
    }
 }   
 post{
    failure{
        echo '❌ Pipeline Failed'
    }
 }
}