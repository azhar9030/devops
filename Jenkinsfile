pipeline {
  agent any
  stages {
    stage('code build') {
      steps {
	sh 'echo "code build is initialising"'
	sh "docker build -f Dockerfile -t test02.osdemo.com:5000/httpd-image ."
	sh "docker image push test02.osdemo.com:5000/httpd-image"
        sh 'echo "successfully built docker image"'
      }
    stage('Docker build') {
      steps {
	sh 'echo "docker build is initialising"'
	sh "docker build -f Dockerfile -t test02.osdemo.com:5000/httpd-image ."
	sh "docker image push test02.osdemo.com:5000/httpd-image"
        sh 'echo "successfully built docker image"'
      }	    
    }
  }
}
