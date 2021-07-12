pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
    }
    post{
        steps{
                    build job: 'testpipeline2', parameters:[string(name:'STR_VAL',value:'the name')]
    }
}