#!groovy
@Library('shared-pipeline@master') _

pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                myEcho()
                echo 'This is the build stage'
            }
        }
        stage('Test') { 
            steps {
                echo 'This is the test stage'
            }
        }
        stage('Deploy') { 
            steps {
                echo 'This is the deploy stage'
            }
        }
    }
}
