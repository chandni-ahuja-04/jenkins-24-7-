pipeline {
    agent any
stages {
        stage('Clone GitHub Repo') {
            steps {
                git 'https://github.com/chandni-ahuja-04/jenkins-24-7-.git'
            }
        }

        stage('Copy Folder to Remote Server') {
            steps {
                sh '''
                echo "Sending folder to remote server..."
                scp -r -i chandni.pem ~/jenkins-24-7-/om/ ubuntu@54.208.18.40:/home/ubuntu/
                '''
            }
        }
    }
}
