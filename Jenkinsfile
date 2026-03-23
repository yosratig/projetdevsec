pipeline {
    agent {
        docker {
            image 'node:20' // image officielle Node.js
            args '-u root:root' // optionnel, pour avoir les droits suffisants
        }
    }

    stages {
        stage('Build & Test') {
            steps {
                echo '🛠️ Installation des dépendances et tests...'
                sh 'npm install'
                sh 'npm test'
            }
        }
    }

    post {
        success {
            echo '✅ Build & Tests réussis !'
        }
        failure {
            echo '❌ Build ou Tests échoués !'
        }
    }
}
