
pipeline {
    agent any
    tools{
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    environment {
        SNAP_REPO = 'CI-Jenkins-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin123'
        RELEASE_REPO = 'CI-Jenkins-release'
        CENTRAL_REPO = 'CI-Jenkins-meven-central'
        NEXUSIP = '172.31.9.47'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'CI-Jenkins-group'
        NEXUS_LOGIN = 'nexuslogin'

    }

    stages{
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}
