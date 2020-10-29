pipeline {
    agent any
        
    stages {
		stage('Release') {
			when {
					expression {
						isRelease = (env.BRANCH_NAME ==~ /^(?:.*release\/\w+).*$/)
						echo "isRelease: ${isRelease}"
						return isRelease
					}
			}
            steps {
                echo 'This is stage for Release branch.'
            }
		}
        stage('Integration') {
            when {
					expression {
						isIntegration = (env.BRANCH_NAME ==~ /^(?:.*integration\/\w+).*$/)
						echo "isIntegration: ${isIntegration}"
						return isIntegration
					}
			}
            steps {
                echo 'This is stage for Integration branch.'
            }
        }
    }
}