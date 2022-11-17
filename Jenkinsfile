pipeline {
    agent {
  label 'node'
}
stages {
    stage ('git') {
        steps {
            git branch: 'main',
            url: 'https://github.com/bharathireddygithub/spring-petclinic.git'
        }
       
    }
     stage ('build') {
            steps {
                sh 'mvn package'
            }
            
        }
        stage ('artifactory') {
            steps {
                archiveArtifacts artifacts: '**/target/*.jar'
            
            }
        }
        stage ('test repots') {
            steps {
                 junit '**/target/surefire-reports/*.xml'
            }
        }
}
}