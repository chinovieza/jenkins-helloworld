pipeline {

    agent any

    environment {
        PROJECT_PATH="/var/jenkins_home/workspace/TEST"
    }

    stages{
        stage('Pull the products config from Git') {
            steps {
                dir("${PROJECT_PATH}") {
                    sh """
                    echo "Hello World"
                    pwd
                    ls -alF
                    """
                }
            }
        }
    }
}