pipeline {
    agent any
    triggers {
        cron('* * * * *')
    }
    stages {
        stage('exemple') {
            steps {
                echo 'Bonjour le monde'
            }
        }
    }
}