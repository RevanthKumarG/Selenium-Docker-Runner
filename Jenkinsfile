pipeline{
	agent any
	stages{

		stage("Start Grid"){
			steps{
			  bat "docker-compose up -d hub chrome firefox"
			}
		}
		stage("Run Test"){
			steps{
				bat "docker-compose up searchmodule bookflightmodule"
			}
		}

		stage("Stop Grid"){
			steps{
				bat "docker-compose down"
			}
		}
	}
	
}