
pipeline {
agent { label "jenkins-docker"}
environment{
DOCKERHUB_CREDENTIALS = credentials(ibrahima12-docckerhub')
}
stages {
stage ('Build') {
steps {
sh 'docker .......'
}
}
stage ('Login') {
steps {
sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u
$DOCKERHUB_CREDENTIALS_USR --password-stdin'
}}
stage ('Push') {
steps {
sh 'docker .......'
}
}
}
}
