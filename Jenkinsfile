pipeline {
    agent any

    stages {
        echo 'hello'
        stage ('Compile') {
            steps {
                withMaven(maven : 'maven') {
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
