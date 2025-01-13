pipeline{
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
 
    stages{
        stage('build'){
            steps{
                echo "build"
            }
        }

        stage('deployment production'){
           when{
            allOf {
                branch 'master'
                environment name: 'DEPLOY_TO', value: 'production'
            }
           }
            steps{
                echo 'deploy'
            }
        }
    }
    post{
        always {
            echo 'always ...'
        }
        success {
            echo 'success !'
        }
    }
}