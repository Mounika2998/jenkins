pipeline {
    agent any
    environment {                                       // Declaring at pipeline will allow all the stages to access this variable
        ENV_URL  = "pipeline.global.com"
        
    }


    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                echo 'ENV_URL is ${ENV_URL}'
            }
        }
    }
}
