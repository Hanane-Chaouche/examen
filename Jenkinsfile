pipeline {
    agent any

    stages {
        stage('Vérifier l\'environnement') {
            steps {
                echo '🔍 Affichage des versions et variables'
                bat 'echo %PATH%'
                bat 'java -version'
                bat 'python --version'
            }
        }

        stage('Exécuter les scripts') {
            steps {
                echo '🚀 Exécution du script Python'
                bat 'python hello.py'

                echo '🛠️ Compilation et exécution du programme Java'
                bat 'javac HelloWorld.java && java HelloWorld'
            }
        }
    }
}
