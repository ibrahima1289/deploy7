
pipeline {
  agent { label "jenkins-docker"}
  environment{
    DOCKERHUB_CREDENTIALS = credentials('ibrahima12-dockerhub')
  }
  stages {
      stage ('Build') {
          steps {
              sh '''docker build -t ibrahim12/deploy7-java .'''
          }
      }
      stage ('Login') {
          steps {
               sh '''echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'''
          
          }
      }
      stage ('Push') {
          steps {
               sh '''docker push ibrahim12/deploy7-java:latest'''
          }
      }
  }
}
