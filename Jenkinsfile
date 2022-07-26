pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                sh './gradlew npm_start'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
