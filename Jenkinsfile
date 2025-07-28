pipeline {
    agent { label 'Windows_11_Home' }

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repo...'
            }
        }

        stage('Run Script') {
            steps {
                bat 'python3 hello.py'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '**/*.py', fingerprint: true
            }
        }
    }
}
