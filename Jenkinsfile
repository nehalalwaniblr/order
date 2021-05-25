pipeline {
    agent any
    environment {
        PATH = "/opt/apache-maven-3.10/bin:$PATH"
    }
    tools {
        maven 'maven-3.10'
        jdk 'jdk8'
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
                sh 'mvn -B -DskipTests clean package'
            }

        }
    }
}
