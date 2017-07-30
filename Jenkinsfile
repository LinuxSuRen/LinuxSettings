pipeline {
    agent any
    
    environment {
        DEPLOY = 'false'
    }
    
    stages {
        stage('Test') {
            steps {
                echo 'test'
            }
        }
    }
}

properties([
    [
        $class: 'GithubProjectProperty',
        displayName: '',
        projectUrlStr: 'https://github.com/LinuxSuRen/'
    ],
    buildDiscarder(
        logRotator(artifactDaysToKeepStr: '',
        artifactNumToKeepStr: '',
        daysToKeepStr: '7',
        numToKeepStr: '70')
    ),
    pipelineTriggers([])
])
