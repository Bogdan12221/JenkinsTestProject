pipeline {
    agent any
    
    stages {
        stage('Ok') {
            steps {
                echo "Ok"
            }
        }
		stage('Build') {
            steps {
                echo "Build"
				bat "dotnet build" 
            }
        }
    }
    post {
        always {
            emailext body: '$PROJECT_NAME - Build # $BUILD_NUMBER - $BUILD_STATUS: Check console output at $BUILD_URL to view the results.',
							recipientProviders: [[$class: 'DevelopersRecipientProvider'], 
							[$class: 'RequesterRecipientProvider']], 
							subject: '$PROJECT_NAME - Build # $BUILD_NUMBER - $BUILD_STATUS!'
        }
    }
}