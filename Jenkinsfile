pipeline {
    agent any
    stages {
        stage("clone the code") {
            steps {
                git "https://github.com/vinitkumargoel/jenkin_l1" 
            }
        }
        stage('Compile') {
            steps {
                sh "'javac' JavaProgram.java"
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'JavaProgram.class'
        }
    }
}
