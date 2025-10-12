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
                yum install httpd -y
                systemctl enable httpd
                systemctl start httpd
                systemctl status httpd
                cp index.html /var/www/html
                '''
            }
        }
    }
    

}
