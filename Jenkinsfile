pipeline {

    agent any

    environment {
        PROJECT_PATH="/var/jenkins_home/workspace/My-Pipeline_main"
    }

    stages{
        stage('Pull the products config from Git') {
            steps {
                dir("${PROJECT_PATH}") {
                    sh """
                    echo "Hello World"
                    pwd
                    ls -alF
                    git branch
                    git checkout master
                    git branch
                    """
                }
            }
        }
    }
}