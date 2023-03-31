pipeline {
    agent any
    environment {                                       // Declaring at pipeline will allow all the stages to access this variable
        ENV_URL  = "pipeline.global.com"
        SH_CRED = credentials('SSH_CRED') 
        
    }


    stages {
        stage('Hello from stage 1') {
            steps {
                echo 'Hello World'
                echo 'ENV_URL is ${ENV_URL}'
            }
        }

        stage('Three') {
            steps{

                sh '''
                            echo Hello World
                            echo Hai World
                            echo I am using Pipeline Syntax Generator
                            sleep 300
                            env
                        '''
            }
        }


        
    }
}
