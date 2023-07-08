pipeline {
    agent {
        docker {
            image 'my-docker-image:rev1.0'
            // You can also specify additional Docker run options if needed
        }
    }
    stages {
        stage('Build') {
            steps {
                // Add your build steps here
                sh 'docker build -t my-docker-image .'
            }
        }
        stage('Test') {
            steps {
                // Add your test steps here
                sh 'docker run -itd --name=my-container my-docker-image bash'
            }
        }
    }
}
