pipeline {
    agent { node { label 'slave'} }
    environment {
        TEST_URL = "google.com"
        SSH = credentials('centos-ssh')
    }
    options {
        ansiColor('xterm')
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    triggers {
        pollSCM('*/1 * * * *')
    }
    tools {
        maven 'maven'
    }
    stages {
        stage('compile') {
            when {
                branch 'production'
            }
            input {
                message "Should we continue?"
                ok "Yes, we should."
            }
            steps {
                echo TEST_URL
                echo SSH
                sh 'env'
                sh 'mvn --version'
            }
        }
        stage('compile') {
            when {
                branch 'test'
            }
            steps {
                echo TEST_URL
                echo SSH
                sh 'env'
                sh 'mvn --version'
            }
        }
    }
    post {
        always {
            echo 'post'
        }
    }
}