pipeline {
    agent none
    stages {
        stage('Build web') {
            agent {
                dockerfile {
                    additionalBuildArgs '-t web'
                }
            }
            steps {
                sh 'echo web built'
            }
        }
    }
}