pipeline {
    agent any

    environment {
        MAVEN_HOME = '/Users/gowe/Downloads/apache-maven-3.5.0'  // Specify the Maven installation directory
        PATH = "${MAVEN_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Compile Stage') {
            steps {
                script {
                    sh 'mvn clean compile'
                }
            }
        }

        stage('Testing Stage') {
            steps {
                script {
                    sh 'mvn test'
                }
            }
        }

        stage('Install') {
            steps {
                script {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
