pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        sh 'echo "Hello World"'
        withAWS(region:'us-west-2', credentials:'aws-static' ){
          s3Upload(file:'index.html', bucket:'jenkinspipelinesS3', path:'')
        }
      }
    }
  }
}
