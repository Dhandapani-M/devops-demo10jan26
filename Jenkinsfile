pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'git@github.com:Dhandapani-M/devops-demo10jan26.git'
            }
        }

        stage('Deploy to Nginx') {
            steps {
                sh '''
                  echo "Deploying index.html to Nginx..."
                  sudo cp index.html /var/www/html/index.html
                  sudo systemctl restart nginx
                '''
            }
        }
    }
}

