node {
    try {

        stage('Build') {
            sh '''
            echo "Building Java project..."
            cd "Password Protection"
            mkdir -p build
            javac -d build src/*.java
            echo "Build successful"
            '''
        }

        stage('Test') {
            sh '''
            echo "Running test stage..."
            '''
        }

        stage('Deploy') {
            sh '''
            echo "Packaging application..."
            cd "Password Protection"
            jar cf FileEncrypter.jar -C build .
            echo "Artifact created"
            '''
        }

        echo "Pipeline executed successfully!"

    } catch (Exception e) {
        echo "Pipeline failed!"
        throw e
    }
}
