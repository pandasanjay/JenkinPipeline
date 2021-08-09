pipeline {
    agent any 
    triggers {
        issueCommentTrigger('.*Build.*')
    }
    stages {
        stage('Build') { 
            steps {
                sh 'echo "Build"' 
            }
        }
        stage('Test') { 
            steps {
                 sh 'echo "Test 6"'
            }
        }
        stage('Deploy') { 
            steps {
                 sh 'echo "Deploy"'
            }
        }
    }
}
