pipeline {
    agent any
    environment {
        ENV_URL = pipeline.google.com
    }
    
    stages {
        stage(" stage one ") {
            steps{
                sh ''' echo stage one profile 
                       echo environemt url ${ENV_URL}
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