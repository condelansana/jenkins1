pipeline{
    agent any
    
    stages{
        stage('build'){
            failFast true
            parallel {
                stage('build frontend'){
                    steps{
                        echo "build"
                    }
                }
                stage('build backend'){
                        steps{
                            echo "build"
                        }
                }
            }
        }
        
        stage('deployment production'){
            steps{
                echo 'deploy'
            }
        }
    }
}