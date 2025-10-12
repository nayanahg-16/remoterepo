pipeline{
    agent{
        label 'slave'
    }

    stages{
        stage('hostanme'){
            steps{
                sh 'hostname'
            }
        }

         stage('status'){
            steps{
                sh '''
                systemctl status httpd
                cp index.html /var/www/html
                '''
            }
        }
    }
    

}
