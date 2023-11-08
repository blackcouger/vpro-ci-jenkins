pipeline{
    agent any
    tools{
        maven "maven3"
        jdk "oraclejdk8"
    }
    environment{
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin123'
        RELEASE_REPO= 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUSIP '52.87.230.105'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
        
    }
    stages{
        stage('Build'){
            steps{
                sh 'mvn -s settings.xml -Dskiptest install'

            }
        }
    }
}