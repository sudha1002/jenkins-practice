pipeline {
    agent { label 'AGENT-1'}
    environment { 
        PROJECT = 'EXPENSE'
        COMPONENT = 'BACKEND'

    }
    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                     echo "hello, this is build"
                     echo "project: $PROJECT"
                    """ 

                }
                
            }
        }
        stage('Test') {
            steps {
                script{
                    sh """
                     echo "hello, this is test"
                    """
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                    sh """
                     echo "hello, this is deploy"
                    """
                }
                
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'I will run when pipeline is failed'
        }
        success { 
            echo 'I will run when pipeline is success'
        }
    }
}