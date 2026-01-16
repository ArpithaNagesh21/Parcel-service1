pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                sh '''
                echo "Cloning repository..."
                rm -rf Parcel-service1
                git clone https://github.com/ArpithaNagesh21/Parcel-service1.git
                 ''' 
            }
        }

        stage('Build & Test') {
            steps {
                sh '''
                export JAVA_HOME=$(dirname $(dirname $(readlink -f $(which java))))
                echo $JAVA_HOME
                export PATH=$JAVA_HOME/bin:$PATH
                '''
            }
        }
      stage ('Deploy') {
          steps {
              sh '''
              mvn clean install
              whoami
              // mvn spring-boot:run
              '''
    }
}
    }
}

  
