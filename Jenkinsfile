pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/smadala8095/smd.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
         stage('Compile Java') {
            steps {
                sudo sh  'javac src/main/java/com/example/SimpleJavaApp.java'
            }
        }
        stage('Run Java Application') {
            steps {
              sudo   sh  'java src/main/java/com/example/SimpleJavaApp'
            }
        }
    }
}

