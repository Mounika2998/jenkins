pipeline {
    agent any
    environment {                                       // Declaring at pipeline will allow all the stages to access this variable
        ENV_URL  = "pipeline.global.com"

    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }


    stages {
        stage('Hello from stage 1') {
            steps {
                sh "echo Hello World"
                sh "cat /home/centos/file.txt"
                sh "echo ENV_URL is ${ENV_URL}"
            }
        }

        stage('Three') {
            steps{

                sh '''
                            echo Hello World
                            env
                        '''
            }
        }


        
    }
}
