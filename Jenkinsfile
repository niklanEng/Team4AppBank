pipeline{
	agent {
		label 'slave1'
	}
	stages{
		stage('1-clone'){
			steps{
				sh 'lscpu'
			}
		}
		stage('2-codebuild'){
			agent {
				label 'slave2'
			}
			steps{
				sh 'df -h'
			}
		}
		stage('3-codetest'){
			agent{
				lable 'slave2'
			}
			steps{
				sh '/etc/passwd/'
			}
		}
		stage('4-checkout'){
			agent {
				label 'slave1'
			}
			steps{
				echo "Welcome to Etech"
			}
		}
	}
}