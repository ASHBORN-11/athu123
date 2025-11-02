https://github.com/rubenlagus/TelegramBots  // for maven 

https://github.com/bonigarcia/selenium-jupiter.git // for selenium 

code for pipeline q8 : 

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


code for pipeline q16 :

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Compiling Java Program...'
                bat 'javac athu.java'
            }
        }
        stage('Run') {
            steps {
                echo 'Running the Program...'
                bat 'java athu'
            }
        }
    }
}


java code : 
public class athu {
    public static void main(String[] args) {
        System.out.println("Hello, Jenkins!");
    }
}

