pipeline {
  agent any
  stages {
    stage ('Upload to AWS') {
      steps {
        withAWS(region:'eu-west-3', credentials:'aws-static') {
          sh 'echo "Uploading content with AWS creds"'
          s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'udacity-project-3')
        }
      } 
    }
  }
}
