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
                sh "cp  /root/.jenkins/workspace/pipeline2/target/my-app-1.0-SNAPSHOT.jar /opt/apache-tomcat-9.0.14/webapps"
            }
        }
    }
}
