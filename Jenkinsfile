pipeline{
    agent any
    tools {nodejs "Node 18.8"}
    
    stages {
        stage('source'){
            steps{
                git 'https://github.com/sd031/aws_codebuild_codedeploy_nodeJs_demo.git'
            }
        }
    
        stage ('build'){
            steps{
                sh 'npm install'
            }
        }
    }
}
