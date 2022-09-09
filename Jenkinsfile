pipeline{
    agent any    
    stages {
        stage('source'){
            steps{
		checkout([$class: 'GitSCM', branches: [[name: '*/Deployment']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/sd031/aws_codebuild_codedeploy_nodeJs_demo.git']]])
		sh 'cat index.js'
            }
        }
	stage('Deploy to aws ec2'){
            steps{
                sshagent(credentials :['52.87.233.180']){
                    sh 'ssh -o StrictHostKeyChecking=no ubuntu@ec2-52-87-233-180.compute-1.amazonaws.com uptime'
                    sh 'ssh -v ubuntu@ec2-52-87-233-180.compute-1.amazonaws.com'
                    sh 'scp -r /var/lib/jenkins/workspace/DeploymentTest1 ubuntu@ec2-52-87-233-180.compute-1.amazonaws.com:/home/ubuntu'
                }
            }
        }
    }
}
