pipeline {
    agent any
    environment {                                       // Declaring at pipeline will allow all the stages to access this variable
        ENV_URL  = "pipeline.global.com"
        
    }


    stages {
        stage('Hello from stage 1') {
            steps {
                echo 'Hello World'
                echo 'ENV_URL is ${ENV_URL}'
            }
        }

        stage('Hello from stage 2') {
            ENV_URL=pipeline.stage.com
            steps {
                echo 'Hello World'
                echo 'ENV_URL is ${ENV_URL}'
            }
        }
    }
}
