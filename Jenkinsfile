pipeline {
    agent any 
    triggers {
        issueCommentTrigger('.*Build.*')
    }
    stages {
        stage('print env vars') {
            steps {
                sh 'printenv'
            }
        }
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
            when { not {environment name: 'GITHUB_COMMENT', value: 'Build'} }
            steps {
                 sh 'echo "Deploy"'
            }
        }
    }
}
