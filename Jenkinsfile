pipeline {
    agent any
    
    parameters {
        booleanParam(name: 'INCLUDE_PROD_TESTS', defaultValue: false, description: "verification de l'inclusin des tests")
        choice(name: 'CHOICES', choices: ['dev', 'prod', 'deux'], description: 'environnement')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test - Dev Environment') {
            // environment {
            //     DEPLOY_TO = "development"
            // }
            when {
                anyOf{
                    // environment name: 'DEPLOY_TO', value: 'development';
                    equals expected: 'dev' || 'deux', actual: params.CHOICES;
                    // expression { return params.INCLUDE_PROD_TESTS }
                }
            }
            steps {
                echo 'Testing in dev environment...'
            }
        }
        stage('Test - Prod Environment') {
            //  environment {
            //     DEPLOY_T = "production"
            // }
            when {
                allOf {
                    // environment name: 'DEPLOY_TO', value: 'production';
                    // equals expected: 'prod' || 'deux', actual: params.CHOICES;
                    // expression { return params.INCLUDE_PROD_TESTS }
                    equals expected: true, actual: params.INCLUDE_PROD_TESTS
                }
            }
            steps {
                echo 'Testing in prod environment...'
            }
        }
        stage('Deploy') {
            when {
                not {
                    triggeredBy cause: "UserIdCause", detail: "joe"
                }
            }
            steps {
                echo 'Deploying...'
            }
        }
    }
}


// pipeline {
//     agent any
//     stages {
//         stage('Déploiement') {
//             when {
//                 beforeInput true
//                 branch 'main'
//             }
//             input {
//                 message "Déployer en production ?"
//                 id "input-deploiement"
//             }
//             steps {
//                 echo 'Déploiement en cours'
//                 echo 'Déploiement en cours'
//             }
//         }
//     }
// }



// pipeline {
//     agent none
//     environment {
//         DEPLOY_TO = "production"
//     }
//     stages {
//         stage('Déploiement') {
//             // agent { label 'my-label' }
//             agent any
//             when {
//                 beforeAgent true
//                 environment name: 'DEPLOY_TO', value: 'production'
//             }
//             steps {
//                 echo 'Déploiement en cours'
//             }
//         }
//     }
// }









// pipeline {
//     agent any
//     stages {
//         stage('Build et Test') {
//             steps {
//                 echo 'Build et Test'
//             }
//         }
//         stage('Déploiement en Production') {
//             input {
//                 message "Voulez-vous déployer en production ?"
//                 ok "Oui, déployons."
//                 submitter "admin,devops"
//                 submitterParameter "USER_SUBMIT"
//                 parameters {
//                     string(name: 'VERSION', defaultValue: 'latest', description: 'Quelle version souhaitez-vous déployer ?')
//                 }
//             }
//             steps {
//                 echo "Déploiement de la version ${VERSION} en production."
//                 echo "user : ${USER_SUBMIT}"
//                 echo "version : ${VERSION}"
//                 // Votre code pour le déploiement
//             }
//         }
//     }
// }