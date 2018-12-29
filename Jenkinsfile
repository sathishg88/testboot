pipeline {
    agent any
    tools {
        maven 'maven-3.3.3' 
        jdk 'jdk1.7.0_45'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

        stage ('Build') {
            steps {
                sh 'mvn -Dmaven.test.failure.ignore=true install' 
            }
            
        }
    }
}
