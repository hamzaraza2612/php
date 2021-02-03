pipeline {
    agent any 
    stages {
        stage('run node') { 
            steps {
                echo 'execute node'
                nodejs('Node-10.1') {
                    sh 'yarn install'
                }
            }
        }
        stage('run gradle') { 
            steps {
                echo 'execute gradle'
                withGradle() {
                    sh './gradle -v'
                }
            }
        }
        
    }
}
