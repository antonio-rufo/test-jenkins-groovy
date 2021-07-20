#!/usr/bin/env groovy

@Library('lto-jenkins-pipeline-library@master') _

pipeline {
    agent none
    environment {
        APP_TYPE = "test-microservice-utilities"
        APP_VERSION = setVersion(true)
    }
    options {
        buildDiscarder(
            logRotator(numToKeepStr: '100', daysToKeepStr: '30', artifactNumToKeepStr: '20', artifactDaysToKeepStr: '10')
        )
        timestamps()
    }
    stages {
        stage("Checkout localBranch") {
            steps {
                sh "git config remote.origin.fetch '+refs/heads/*:refs/remotes/origin/*'"
                sh "git fetch --all"
                sh "echo Hello World"
            }
        }
    }
}
