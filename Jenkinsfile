pipeline {
    agent any

    stages {
        stage('validate') {
            steps {
                echo 'building..'
                sh '/usr/share/maven/bin/mvn validate'
            }
        }
        stage('build') {
            steps {
                echo 'Testing..'
                   sh '/usr/share/maven/bin/mvn package'
            }
        }
        stage('test') {
            steps {
                echo 'Deploying....'
   sh '/usr/share/maven/bin/mvn test'
            }
        }
    }
}
