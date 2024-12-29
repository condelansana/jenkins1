pipeline{
    agent any
    stages{
        stage('build'){
            options{
                timestamps()
            }
            steps{
                sh 'npm -v'
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