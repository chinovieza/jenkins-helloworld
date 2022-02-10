pipeline {

    agent any

    environment {
        PROJECT_PATH="/home/jenkins/myaccount"
    }

    stages{
        stage('Pull the products config from Git') {
            steps {
                dir("${PROJECT_PATH}") {
                    sh """
                    git reset --hard HEAD
                    git checkout master
                    git pull origin master
                    git fetch --tags --force
                    if [ "${params.VERSION}" != "latest" ]; then git checkout "${params.VERSION}"; fi
                    """
                }
            }
        }
    }
}