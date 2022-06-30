pipeline {
    agent any
    stages {
        stage('Submit Stack') {
            steps {
            sh "aws cloudformation create-stack --stack-name my_vpc --template-body file://vpc.json --region 'us-east-1'"
              }
             }
            }
            }
