pipeline {

    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'gradle clean build'
            }
        }
        stage('Delivery') {
            steps {
                sh 'aws s3 cp build/libs/CompactDiscNoDatabaseBoot-0.0.1-SNAPSHOT.jar s3://training.conygre.com/allstate/compactdiscs.jar --region eu-west-1'
            }
        }
        
    }
}