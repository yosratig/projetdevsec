pipeline {
    

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
