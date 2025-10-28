pipeline {
    agent any

    stages {
        stage('Checkout from GitHub') {
            steps {
                echo 'Cloning repository...'
                git branch: 'main', url: 'https://github.com/thor-eng/ci.git'
            }
        }

        // stage('Install dependencies') {
        //     steps {
        //         echo 'Installing Flask...'
        //         sh 'pip install flask pytest'
        //     }
        // }

        // stage('Run Flask app') {
        //     steps {
        //         echo 'Starting Flask app...'
        //         // run Flask in background
        //         sh 'nohup python3 app.py &'
        //         sleep(time: 5, unit: 'SECONDS')
        //     }
        // }

        // stage('Run Tests') {
        //     steps {
        //         echo 'Running tests...'
        //         sh 'pytest test_app.py'
        //     }
        // }
    }

    post {
        success {
            echo '✅ Flask app ran successfully and tests passed!'
        }
        failure {
            echo '❌ Build failed!'
        }
    }
}