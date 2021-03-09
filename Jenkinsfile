pipeline {
   agent any
       stages {
        stage('Build') {
            steps {
                sh "mvn clean install"
            }
        }
        stage('test') {
            steps {
                sh "mvn test"
            }
        }
        stage('Deploy') {
            steps {
                sh "cp -R /root/.jenkins/workspace/exp_pipeline/target/* /opt/apache-tomcat-8.5.3/webapps"
            }
        }       
    }
}
