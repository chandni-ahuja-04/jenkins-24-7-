pipeline {
    agent any
stages {
        stage('Clone GitHub Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/chandni-ahuja-04/jenkins-24-7-.git'
            }
        }

        stage('Copy Folder to Remote Server') {
            steps {
                sh '''
                echo "Sending folder to remote server..."
                scp -i chandni.pem -r /home/ubuntu/jenkins-24-7-/om/ ubuntu@54.208.18.40:/home/ubuntu/
                '''
            }
        }
    }
}
