pipeline {
  agent any
  stages {
    stage('build docker image') {
      steps {
        sh '''sh "eval \\$(aws ecr get-login --no-include-email --region us-east-1) && sleep 2"
                sh "cd vote && docker build . -t 635145294553.dkr.ecr.us-east-1.amazonaws.com/node-app:\\${BUILD_NUMBER}"
                sh "docker push 623396122653.dkr.ecr.us-east-1.amazonaws.com/c7-task2/node-app:\\${BUILD_NUMBER}"'''
      }
    }

  }
}