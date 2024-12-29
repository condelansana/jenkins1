pipeline{
    agent any
    triggers {
            cron(*****)
    }
    parameters{
        string(name: 'NAME', defaultValue: 'M. Jenkins', description: 'Qui est ce ?')
        text(name: 'TEXT', defaultValue: 'un texte', description: 'une description')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'true ou false')
        choice(name: 'CHOICE', choices: ['un', 'deux', 'trois'], description: 'une liste de choix')
        password(name: 'PASSWORD', description: 'un mot de passe')

    }
  
    stages{
        stage('build'){
            options{
                timestamps()
            }
            steps{
                echo "NAME: ${ NAME}"
                echo "TEXT: ${ TEXT}"
                echo "TOGGLE: ${ TOGGLE}"
                echo "CHOICE: ${ CHOICE}"
                echo "PASSWORD: ${ PASSWORD}"
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