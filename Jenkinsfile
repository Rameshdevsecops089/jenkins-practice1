pipeline {
    agent  {
        label 'AGENT-1'
    }
    options {
        timeout(time: 30, unit: 'MINUTES') 
        disableConcurrentBuilds()
    }
    // Build
    stages {
        stage('Build') {
            steps {
                script{
                    sh"""
                        echo "Hello Build"
                        env
                    """    
                }
            }
        }
        stage('Test') {
            steps {
                script{
                    sh"""
                        echo "Hello Testing"
                        env
                    """    
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                    sh"""
                        echo "Hello Deploying"
                        env
                    """    
                }
            }
        }
    }

    post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success{
            echo 'Hello Success'
        }
        failure{
            echo 'Hello failure'
        }
    }
}