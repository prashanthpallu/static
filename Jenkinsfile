pipeline{
  agent any
  stages{
    stage("Upload to AWS"){
      steps {
        sh 'echo "Upoading to AWS Bucket"'
        withAWS(region:'us-west-2', credentials:'aws-static') {
          s3Upload(file:'index.html', bucket:'udacity-static-pallup', path:'index.html')
        }
   }
  }
 }
}
