pipeline {
  agent {
    kubernetes {
      yaml """
apiVersion: v1
kind: Pod
metadata:
  labels:
    repository: testrepository
spec:
  containers:
  - name: ubuntu
    image: ubuntu
    command:
    - cat
    tty: true
"""
    }
  }
  stages {
    stage('Hello World') {
      steps {
        container('ubuntu') {
          sh 'echo "Hello World"'
        }
      }
    }
  }
}