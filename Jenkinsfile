pipeline {
    agent any

    environment {
        JAVA_HOME = tool name: 'JDK11'  // Ensure JDK 11 is configured in Jenkins
        PATH = "${env.JAVA_HOME}/bin:${env.PATH}"
    }

    stages {

        stage('Checkout') {
            steps {
                echo "Cloning repository..."
                git url: 'https://github.com/ArpithaNagesh21/Parcel-service1.git', branch: 'feature1'
            }
        }

        stage('Build & Test') {
            steps {
                echo "Building and testing the project..."
                sh 'mvn clean install'
            }
        }

    }

    post {
        success {
            echo '✅ Build and test completed successfully.'
        }
        failure {
            echo '❌ Build failed. Check the logs.'
        }
    }
}
