pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                sh "mvn clean"
            }
        }
        stage('--test--') {
            steps {
                sh "mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "mvn package"
            }
        }
        stage('--deploy--') {
            steps {
                sh "cp  /root/.jenkins/workspace/pipeline2/target/MYAPP-8.0.jar /opt/apache-tomcat-9.0.14/webapps"
            }
        }
    }
}
