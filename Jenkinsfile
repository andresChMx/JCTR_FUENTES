pipeline {
    agent any
    tools { 
        maven 'MAVEN_3_6_0' 
        jdk 'JDK_1_8' 
    }
	
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'MAVEN_3_6_0') {
                    bat 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'MAVEN_3_6_0') {
                    bat 'mvn test'
                }
            }
        }


        stage ('package Stage') {
            steps {
                withMaven(maven : 'MAVEN_3_6_0') {
                    bat 'mvn package'
                }
            }
        }
    }
}