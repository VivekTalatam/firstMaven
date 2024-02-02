pipeline {
    agent any
tools{
    Maven 'Maven 3.9.6'
}
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_9_6') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_9_6') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_9_6') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
