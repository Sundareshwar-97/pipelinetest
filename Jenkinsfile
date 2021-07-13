pipeline {
    agent any
    stages {
        stage('Python execution') {
            steps {
                echo 'executing python'
                sh 'python3 pyscript.py'
            }
            stage('shell execution') {
                steps {
                    echo 'executing shell'
                    sh 'sh "./shscript.sh"'
                }
            }
        }
        post {
            success {
                build job: 'testpipeline1', parameters: [string(name: 'STR_VAL', value: 'the name')]
            }
        }