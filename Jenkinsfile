pipeline {
    agent any

    stages {
        //criar ec2 na aws
        stage('Provisionar Recurso AWS') {
            steps {
                script {
                    withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: '799a3db6-6f2d-4365-aaa5-db71fefbe6ba', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
                        bat '"C:\\Program Files\\Amazon\\AWSCLIV2\\aws" ec2 run-instances --image-id ami-064fff85dd20d65a6 --count 1 --instance-type t2.micro --key-name MyKeyPair --subnet-id subnet-0bcbe820e303288c5 --region us-east-1'
                    }
                }
            }
        }
    }
}



