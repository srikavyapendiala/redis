pipeline {
  agent any

  stages {
    stage('Prepare Artifacts') {
       steps {
       sh '''
         zip -r redis.zip *
       '''
       }
    }
    stage('Upload Artifacts') {
      steps {
       sh '''
       curl -v -u admin:kavya --upload-file redis.zip http://172.31.6.66:8081/repository/redis/redis.zip
       '''
      }
    }
  }
}
