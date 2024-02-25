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
		
		  stage('Build') {
            steps {
                sh 'javac SimpleJavaApp.java'
            }
        }
        stage('Compile') {
            steps {
                sh 'java -cp target/classes com.example.SimpleJavaApp'
            }
        }
    }
}
