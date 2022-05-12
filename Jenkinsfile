pipeline {
    agent any

    stages {
        stage('git cloning') {
            steps {
                git branch: 'main', url: 'https://github.com/jsbloo/jenk-test2'
            }
        }
        stage('run script') {
            steps {
                sh 'chmod +x myscript.sh'
                sh './myscript.sh'
            }
        }
         stage('archive output') {
            steps {
                archiveArtifacts artifacts: 'output.txt', followSymlinks: false
            }
        }
    }
}
