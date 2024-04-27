pipeline {

    agent any

    tools {

        maven "maven3"

        jdk "jdk8"

    }

    environment {

        SNAP_REPO = 'vprofile-snapshot'

        NEXUS_USER = 'admin'

        NEXUS_PASS = 'admin123'

        RELEASE_REPO = 'vprofile-release'

        CENTRAL_REPO = 'vprofile-maven-central'

        NEXUSIP = '172.31.49.29'

        NEXUSPORT = '8081'

        NEXUS_GRP_REPO = 'vprofile-maven-group'

        NEXUS_LOGIN = 'nexuslogin'

    }

    stages {

        stage('build') {

            steps {

                script {

                    sh "mvn -s settings.xml -DskipTests install"

                }

            }

        }

    }

}