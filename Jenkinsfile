pipeline{
    agent any
 
    stages{
        stage('build'){
            steps{
                echo "build"
            }
        }

        stage('deployment production'){
           when{
            branch 'master'
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