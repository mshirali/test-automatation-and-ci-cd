pipeline {
    agent any
    stages {
        stage('Run Tests') {
            steps {
                script {
                    def result = sh(script: 'robot --outputdir results tests/', returnStatus: true)
                    if (result != 0) {
                        error("Tests failed with exit code: ${result}")
                    }
                }
            }
        }
    }
}
