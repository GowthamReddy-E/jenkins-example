pipeline {
    agent any 

    environment {
        MAVEN_HOME = '/opt/apache-maven-3.9.6'
        PATH = "${MAVEN_HOME}/bin:${env.PATH}"
        JAVA_HOME = '/Users/gowe/Library/Java/JavaVirtualMachines/corretto-18.0.2/Contents/Home'
    }

    stages {
        stage('Clean') {
            steps {
                sh 'mvn clean'
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }

        stage('Install') {
            steps {
                sh 'mvn install'
            }
        }

        stage('Deploy') {
            steps {
                sh 'mvn deploy'
            }
        }

        stage('Custom Maven Command') {
            steps {
                sh 'mvn clean '
            }
        }

        // Add more stages as needed...
    }
}
