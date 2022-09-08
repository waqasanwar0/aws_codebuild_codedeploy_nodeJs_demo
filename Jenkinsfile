pipeline{
    agent any
    tools {nodejs "Node 18.8"}
    
    stages {
        stage('source'){
            steps{
                git 'https://github.com/sd031/aws_codebuild_codedeploy_nodeJs_demo.git'
		sh 'cat index.js'
            }
        }
    
        stage ('build'){
            steps{
                sh 'npm install'
            }
        }
    }
}
