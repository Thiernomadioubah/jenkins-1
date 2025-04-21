pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo "L'id du build est ${BUILD_ID}"
                // echo "Le GIT_COMMITTER_EMAIL est ${GIT_COMMITTER_EMAIL}"
                // echo "Le GIT_AUTHOR_EMAIL est ${GIT_AUTHOR_EMAIL}"
                echo "Le JENKINS_URL est ${JENKINS_URL}"
                echo "Le JENKINS_HOME est ${JENKINS_HOME}"
                echo "Le WORKSPACE est ${WORKSPACE}"
                echo "Le WORKSPACE_TMP est ${WORKSPACE_TMP}"
                echo "Le NODE_NAME est ${NODE_NAME}"
                echo "Le JOB_NAME est ${JOB_NAME}"
            }
        }
    }
}
