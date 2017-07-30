pipeline {
    agent any
    
    triggers {
        pollSCM('H/5 * * * *')
    }
    
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
        displayName: 'LinuxSettings',
        projectUrlStr: 'https://github.com/LinuxSuRen/LinuxSettings'
    ],
    buildDiscarder(
        logRotator(
            artifactDaysToKeepStr: '',
            artifactNumToKeepStr: '',
            daysToKeepStr: '7',
            numToKeepStr: '14'
        )
    ),
    pipelineTriggers([])
])
