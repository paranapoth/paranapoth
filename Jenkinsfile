#!/usr/bin/env groovy

node {

    stage('quality analysis') {
        withSonarQubeEnv('sonar') {
            sh "./gradlew sonarqube --no-daemon"
        }
    }

}
