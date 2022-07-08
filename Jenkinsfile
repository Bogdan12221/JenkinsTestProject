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

    }
}