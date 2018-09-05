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

        stage('Build Test Env') {
            agent {
                dockerfile {
                    dir 'tests'
                    additionalBuildArgs '-t test_env'
                }
            }
            steps {
                sh 'echo test env container was built'
            }
        }
        stage('Create network') {
            agent any
            steps {
                sh 'sh ./create_network.sh'
            }
        }


    }
}