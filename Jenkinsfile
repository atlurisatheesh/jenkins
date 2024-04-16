pipeline {
    agent {
        label 'ws'
    }
    environment {
        ENV_URL = " pipeline.google.com "
        SSH_CRED = credentials('SSH_CRED')
    }

    tools {
        maven 'maven-3.8.6' 
    }
    triggers { 
        pollSCM('*/59 * * * *') 
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
                       hsotname
                       sleep 20
                    '''
            }
        }

        stage('Paralle Demo') {
            steps {
                sh ''' echo stage two profile 
                        mvn -v
                        sleep 30
                    '''
            }
        }

        stage(' stage three ') {
            environment {
                BATCH = "satheesh"
            }
            steps {
                sh " echo stage three profile "
                sh "sleep 35"
            }
        }
    }
    // post {
    //     always {
    //         clearWs()
    //     }
    // }


}