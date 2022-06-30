pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name ec2-example --template-body file://01_ec2.yaml --region 'us-east-1'"
              }
             }
            }
            }
