pipeline {
    agent any
    triggers {
  pollSCM('* * * * *')
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello '
                sleep 5
            }
        }
          stage('build') {
            steps {
                echo 'build'
                sleep 5
            }
        }
          stage('test') {
            steps {
                echo 'test'
                sleep 5
            }
        }
          stage('deploy') {
            steps {
                echo 'deploy'
                sleep 4
            }
        }
        stage('create a zip folder'){
            steps{
                sh 'zip -r middleware.zip . -i MIDDLEWARE-SCRIPTS'
            }
        }
        //stage('upload to JFrog'){
          //  steps{
            //    sh 'curl -uadmin:AP8JrETP4pkpQEdKpLHxJwhVieo -T \
              //  <PATH_TO_FILE> \
                //"http://54.236.21.182:8081/artifactory/middeware/<TARGET_FILE_PATH>"'
            //}
       // }
    }
}
