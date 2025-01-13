pipeline{
    agent any
 
    stages{
        stage('build'){
            steps{
                echo "build"
            }
        }

        stage('deplpyment production'){
            input{
                message 'Voulez vous déployer en production'
                ok 'deployer !'
                submitter 'admin, devops'
                submitterParameter 'USER_SUBMIT'
                parameters {
                    string (name: 'VERSION', defautValue: 'latest', description: 'une version')
                }
            }
            steps{
                echo 'user : ${USER_SUBMIT}'
                echo 'version : ${VERSION}'
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