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
                sshagent(['52.87.233.180']){
                    sh '''
                        ssh -o ubuntu@ec2-52-87-233-180.compute-1.amazonaws.com
                    '''
                }
            }
        }
    }
}
