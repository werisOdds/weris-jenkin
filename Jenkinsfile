pipeline {
    agent any
    stages {
        stage('confirm version') {
            steps {
                nodejs('node.17.9.0') {    // <- use node name you configured in “Global Tool Config”.  
                    sh 'node -v'
                    sh 'npm -v'
                }
            }
        }
        stage('install node packages') {
            steps { //ในโปรเจคต้องมี package.json
                nodejs('node.17.9.0') {
                    sh 'npm install'
                    sh 'echo Hello'
                }
            }
        }
    }
}
