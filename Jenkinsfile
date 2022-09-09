pipeline{
    agent any    
    stages {
        stage('source'){
            steps{
		sh 'cat index.js'
            }
        }
	stage('Deploy to aws ec2'){
            steps{
                ssjagent(['52.87.233.180']){
                    sh '''
                        ssh -o StricHostKeyChecking=no ubuntu@ec2-52-87-233-180.compute-1.amazonaws.com ls
                    '''
                }
            }
        }
    }
}
