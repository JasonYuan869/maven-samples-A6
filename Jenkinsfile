pipeline {
  agent any
  tools { 
      maven 'Maven' 
      jdk 'JDK8' 
  }
  
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/JasonYuan869/maven-samples-A6', branch: 'master')
      }
    }
    
    stage('run') {
      steps {
        script {
          sh '''git bisect start 198644632661c67b6c32f59e9047c11a70685e15 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5
          git bisect run mvn clean test'''
        }
      }
    }
    
  }
  
}
