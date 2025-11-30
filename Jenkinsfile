@Library('jenkins-library') _

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                BuildPipeline()
            }
        }
    }

    post {
        always { cleanWs() }
        success { echo "Build completed successfully." }
        failure { echo "Build failed." }
        unstable { echo "Build is unstable." }
    }
}
