pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Cloning the repository into a specific directory
                sh 'git clone https://github.com/smadala8095/smd.git smd_project'
            }
        }
        stage('Build Maven') {
            steps {
                // Navigate to the project directory before executing Maven commands
                dir('smd_project') {
                    sh 'mvn clean package'
                }
            }
        }
        stage('Test') {
            steps {
                dir('smd_project') {
                    sh 'mvn test'
                }
            }
        }
        stage('Compile Java') {
            steps {
                dir('smd_project') {
                    sh 'javac src/main/java/com/example/SimpleJavaApp.java'
                }
            }
        }
        stage('Run Java Application') {
            steps {
                dir('smd_project') {
                    sh 'java -cp target/classes com.example.SimpleJavaApp'
                }
            }
        }
    }
}
