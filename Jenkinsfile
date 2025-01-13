pipeline{
    agent any
    
    parameters {
        booleanParam(name: 'DEPLOY_TO', defaultValue: false, description: 'production ?')
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
                expression { params.DEPLOY_TO }
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