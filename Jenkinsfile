pipeline {
    agent any

    // options { 
    //     timestamps() 
    // }
    stages {
        stage('Example') {
            options {
                timeout(time: 1, unit: 'HOURS')
                timestamps() 
            }
            steps {
                echo 'Hello World'
            }
        }
    }
}