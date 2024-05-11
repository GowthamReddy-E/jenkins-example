pipeline {
    agent any

    environment {
        MAVEN_HOME = '/opt/apache-maven-3.9.6'
        PATH = "${MAVEN_HOME}/bin:${env.PATH}"
        JAVA_HOME = '/Users/gowe/Library/Java/JavaVirtualMachines/corretto-18.0.2/Contents/Home'
    }

    stages {
        stage('Compile Stage') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Testing Stage') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Install') {
            steps {
                sh 'mvn deploy'
            }
        }
    }
}
