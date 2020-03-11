pipeline {
  agent {
    kubernetes {
      yamlFile 'src/main/build/kubernetes-pod.yaml'
    }
  }
  stages {
    stage('Hello World') {
      steps {
        container('ubuntu') {
          sh 'echo Hello World'
        }
      }
    }
  }
}