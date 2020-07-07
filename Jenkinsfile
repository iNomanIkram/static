pipeline {
  agent any
  stages {
  stage('Upload to AWS') {
      steps {
        withAWS(region:'us-east-1',credentials:'nomanikram') {
          s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:udacity-project-3-bucket)
        }
      }
    }
  }
}
