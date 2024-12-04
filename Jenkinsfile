pipeline {   
    agent any 
    tools{
        jdk 'jdk17'
        maven 'maven3'
    }

    stages {
        stage('Git checkout') {
            steps {
                git branch: 'main', credentialsId: 'git-creds' url: 'https://github.com/d3-dhruv/springboot-java-poject.git'
            }
        }
        
        stage('Compile') {
            steps {
                sh "mvn compile"
                 }
        }
        
        stage('Package') {
            steps {
                sh "mvn clean package"
                
                 }
        }
          stage('Maven Test') {
            steps {
               echo 'Maven Test Started'
               sh 'mvn test'
            }
        } 
        
         
    }
}
