pipeline {
    agent any
    parameters {
        string(name: 'PERSONNE', defaultValue: 'M. Jenkins', description: 'À qui devrais-je dire bonjour ?')
        text(name: 'BIOGRAPHIE', defaultValue: '', description: 'Entrez des informations sur la personne')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Activez cette valeur')
        choice(name: 'CHOIX', choices: ['Un', 'Deux', 'Trois'], description: 'Faites un choix')
        password(name: 'MOT_DE_PASSE', defaultValue: 'SECRET', description: 'Entrez un mot de passe')
    }
    stages {
        stage('Exemple') {
            steps {
                echo "Bonjour ${PERSONNE}"
                echo "Biographie : ${BIOGRAPHIE}"
                echo "Toggle : ${TOGGLE}"
                echo "Choix : ${CHOIX}"
                echo "Mot de passe : ${MOT_DE_PASSE}"
            }
        }
    }
}