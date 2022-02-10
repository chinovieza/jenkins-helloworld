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