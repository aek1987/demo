pipeline {

agent any
stages {

stage('init') {
steps {
bat 'mvn clean'
}
}

stage('test') {
steps {
bat 'mvn test'
archiveArtifacts 'target/surefire-reports/*.xml'
}
}

stage('build') {
steps {
bat 'mvn clean package'
archiveArtifacts 'target/*.jar'
}
}

}

}
