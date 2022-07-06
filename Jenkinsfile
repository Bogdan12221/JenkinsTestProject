pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World Changed"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}