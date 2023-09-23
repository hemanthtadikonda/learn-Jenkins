pipeline {
    agent any
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage('compile') {
            steps {
                echo 'Hello World'
            }
        }
        stage('test') {
            steps {
                echo 'Hello World'
            }
        }
        stage('code security') {
            steps {
                echo 'Hello World'
            }
        }
        stage('deploy') {
            steps {
                echo 'Hello World'
            }
        }
        when {
            expression { env.${params.PASSWORD} == admin }
        }
        stage('release') {
            steps {
                echo 'Hello World'
            }
        }

    }
}
