pipeline {
    agent any

    stages {
        stage('Build Steps') {
            steps {
                sh '''
                echo "=== Вміст каталогу ==="
                ls -la

                echo "<p>Build ID: $BUILD_ID</p>" >> index.html

                echo "=== Новий вміст index.html ==="
                cat index.html
                '''
            }
        }
    }
}
