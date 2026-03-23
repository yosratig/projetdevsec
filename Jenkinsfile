pipeline {
    agent any

    stages {
        stage('Build & Test') {
            steps {
                echo '🛠️ Build et tests en cours...'

                // Exemple pour Node.js (comme Juice Shop)
                sh 'npm install'
                sh 'npm test'
            }
        }
    }

    post {
        success {
            echo '✅ Build & Tests réussis ! Phase 1 terminée.'
        }
        failure {
            echo '❌ Build ou Tests échoués ! Pipeline arrêté.'
        }
    }
}
