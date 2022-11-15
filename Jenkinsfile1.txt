pipeline {
    agent any
     environment {
        PROJECT_NAME = "Kriakva"
        OWNER = "Bebra" 
    }
    stages {
        stage('1-Build') {
            steps {
                echo "Start of Stage Build"
                echo "Building......."
                echo "${PROJECT_NAME}"
                echo "${OWNER}"
                sh "echo `pwd`"
                echo "End of Stage Build"
            }
        }
        stage('2-Test') {
            steps {
                echo "Start of Stage Test"
                echo "Testing......."
                sh "echo \$(pwd)"
                 echo "End of Stage Test"
            }
        }
        stage('3-Deploy') {
            steps {
                echo "Start of Stage Deploy"
                echo "Deploying......."
                sh "a=\$(pwd);echo \$a"
                echo "End of Stage Deploy"
            }
        }
    }
}
