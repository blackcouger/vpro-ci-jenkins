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
        NEXUSIP = '172.31.57.89'
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