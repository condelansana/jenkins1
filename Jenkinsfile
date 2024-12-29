pipeline{
    agent any
    options {
        timeout (time: 1, unit: "HOURS")
    }

    stages{
        stage('build'){
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