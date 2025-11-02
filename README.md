https://github.com/rubenlagus/TelegramBots  // for maven 

https://github.com/bonigarcia/selenium-jupiter.git // for selenium 

code for pipeline : 

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'BUILDING THE PROJECT...'
                bat 'echo COMPILING FILES...'
            }
        }
        stage('Test') {
            steps {
                echo 'RUNNING TEST CASES...'
                bat 'echo ALL TESTS PASSED SUCCESSFULLY!'
            }
        }
        stage('Deploy') {
            steps {
                echo 'DEPLOYING PROJECT...'
                bat 'echo DEPLOYMENT SUCCESSFUL!'
            }
        }
    }
    post {
        success {
            echo 'PIPELINE COMPLETED SUCCESSFULLY ✅'
        }
        failure {
            echo 'PIPELINE FAILED ❌'
        }
    }
}
