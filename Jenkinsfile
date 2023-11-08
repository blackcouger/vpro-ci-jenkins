pipeline{
    agent any
    tools{
        maven "maven3"
        jdk "oraclejdk8"
    }
    environment{
        NEXUS_VERSION = "nexus3"
        NEXUS_PROTOCOL = "http"
        NEXUS_URL = "172.31.57.89"
        NEXUSPORT = "8081"
        NEXUS_REPOSITORY = "vprofile-release"
	    NEXUS_REPOGRP_ID    = "vprofile-grp-repo"
        NEXUS_CREDENTIAL_ID = "nexuslogin"
        ARTVERSION = "${env.BUILD_ID}"
        CENTRAL_REPO = "vprofile-release"
        NEXUSIP = "172.31.57.89"
        NEXUS_GRP_REPO = "vprofile-grp-repo"
    }
    stages{
        stage('Build'){
            steps{
                sh 'mvn -s settings.xml -Dskiptest install'

            }
        }
    }
}