pipeline {
    agent any
tools{
    maven 'Maven 3.3.3'
}
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_3_3') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_3_3') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_3_3') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
