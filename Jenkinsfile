pipeline {
     agent { label 'NODE' }
     stages {
        stage('vcs') {
            steps {
             git branch: 'main', 
             url: 'https://github.com/bharathireddygithub/spring-petclinic.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }
        stage( )
     }
}
