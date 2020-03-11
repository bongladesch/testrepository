pipeline {
  agent {
    kubernetes {
      yamlFile 'src/main/build/kubernetes-pod.yaml'
    }
  }
  stages {
    container('ubuntu') {
      stage('Hello World') {
        sh 'echo Hello World'
      }
    }
  }
}