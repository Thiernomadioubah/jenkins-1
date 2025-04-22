// pipeline {
//     agent any
//     triggers {
//         cron('* * * * *')
//     }
//     stages {
//         stage('exemple') {
//             steps {
//                 echo 'Bonjour le monde'
//             }
//         }
//     }
// }

pipeline {
    agent any
    triggers {
        pollSCM('* * * * 1-5')
    }
    stages {
        stage('exemple') {
            steps {
                echo 'Bonjour le monde'
            }
        }
    }
}