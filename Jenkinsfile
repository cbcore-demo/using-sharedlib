#!groovy
@Library('shared-pipeline@master') _

pipeline {
  agent {
    kubernetes {
      label 'mypodtemplate-v1'
      defaultContainer 'jnlp'
      yaml """
apiVersion: v1
kind: Pod
metadata:
  labels:
    some-label: some-label-value
spec:
  containers:
  - name: maven
    image: maven:3.3.9-jdk-8-alpine
    command:
    - cat
    tty: true
"""
    } 
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
