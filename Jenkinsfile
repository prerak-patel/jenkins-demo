pipeline {
    agent any

    stages {
        
        stage ('Compile') {
            steps {
                withMaven(maven : 'maven') {
                    echo 'compiling source code'
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Test') {

            steps {
                withMaven(maven : 'maven') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deploy') {
            steps {
                withMaven(maven : 'maven') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
