pipeline {
    agent any
    environment {
        ENV_URL = " pipeline.google.com "
        SSH_CRED = credentials('SSH_CRED')
    }
    
    parameters {
        string(name: 'PERSON', defaultValue: 'satheesh', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage(" stage one ") {
            environment {
                ENV_URL = " stage.google.com "
                
            }
            steps{
                sh ''' echo stage one profile 
                       echo environemt url ${ENV_URL}
                       env
                    '''
            }
        }
        stage(" stage two ") {
            steps {
                sh " echo stage two profile "
            }
        }
        stage(' stage three ') {
            steps {
                sh " echo stage three profile "
            }
        }
    }


}