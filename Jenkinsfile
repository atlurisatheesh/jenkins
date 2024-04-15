pipeline {
    agent any
    environment {
        ENV_URL = " pipeline.google.com "
        SSH_CRED = credentials('SSH_CRED')
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