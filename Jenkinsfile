pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name my_vpc --template-body file://v1/vpc.json --region 'us-east-1'"
              }
             }
            }
            }
