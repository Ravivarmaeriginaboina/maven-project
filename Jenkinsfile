def output = 'Maven'
def x = '1010'
pipeline {
    agent any
    
    stages {
        stage('checkout') {
            steps {
              git 'https://github.com/saiurakrishna/maven-sample-java-project.git'
              }
        }
        stage('Hello') {
            steps {
                echo "Hello ci/cd World ${output}"
            }
        }
        stage('sample-test') {
            steps {
                echo "Print value ${x}"
            }
        }
        stage('validate') {
          steps {
            sh 'mvn validate'
            }
          }
        stage('compile') {
          steps {
            sh 'mvn compile'
          }
        }
        stage('test') {
          steps {
            sh 'mvn test'
          }
        }
        stage('package') {
          steps {
            sh 'mvn package'
          } 
        }
    }
}
