def x = 6

node  {
    parameters {
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stage('compile code'){
        print 'ok'
    }
    stage('test cases'){
        print 'ok'
    }

    if (x > 10) {
        stage('code quality'){
            print 'ok'
        }
    }else {
        stage('sample'){
            print 'KO'
        }
    }
    stage('code security'){
        print 'ok'
    }
    stage('Release'){
        print 'ok'
    }
}