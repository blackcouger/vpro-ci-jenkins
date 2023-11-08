pipeline{
    agent any
    tools{
        maven "maven3"
        jdk "oraclejdk8"
    }
    environment{
        NEXUS-VERSION = "nexus3"
        NEXUS-PROTOCOL = "http"
        NEXUS-URL = "172.31.57.89:8081"
        NEXUS-REPOSITORY = "vprofile-release"
	    NEXUS-REPOGRP-ID    = "vprofile-grp-repo"
        NEXUS-CREDENTIAL-ID = "nexuslogin"
        ARTVERSION = "${env.BUILD_ID}"
    }
    stages{
        stage('Build'){
            steps{
                sh 'mvn -s settings.xml -Dskiptest install'

            }
        }
    }
}