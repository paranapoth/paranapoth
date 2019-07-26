#!/usr/bin/env groovy

node {
    stage('checkout') {
        checkout scm
    }

    stage('check java') {
        sh "java -version"
    }

    stage('quality analysis') {
        withSonarQubeEnv('sonar') {
            sh "./gradlew sonarqube --no-daemon"
        }
    }
}
