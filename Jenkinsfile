pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                sh '''
                echo "Cloning repository..."
                git clone https://github.com/ArpithaNagesh21/Parcel-service1.git
                 ''' 
            }
        }

        stage('Build & Test') {
            steps {
                sh '''
                sudo apt update
                sudo apt install -y maven
                export JAVA_HOME=$(dirname $(dirname $(readlink -f $(which java))))
                echo $JAVA_HOME
                export PATH=$JAVA_HOME/bin:$PATH
                '''
            }
        }

    }
}
