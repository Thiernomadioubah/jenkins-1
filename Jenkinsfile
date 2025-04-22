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
        pollSCM('H */4 * * 1-5')
    }
    stages {
        stage('exemple') {
            steps {
                echo 'Bonjour le monde'
            }
        }
    }
}