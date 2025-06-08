pipeline { 
    agent any 
    tools { 
        maven 'MVN_HOME' // Ensure name matches configured Maven installation 
    } 
    stages { 
        stage('Checkout') {  
            steps { 
                git branch: 'master', url: 'https://github.com/Gani580/ng5.git'  
            } 
        } 
        stage('Build') {  
            steps { 
                bat 'mvn clean package'  
            } 
        } 
        stage('Test') {  
            steps { 
                bat 'mvn test'  
            } 
        } 
        stage('Run Application') {  
            steps { 
                bat 'java -jar target/veeresh-0.0.1-SNAPSHOT.jar'  
            } 
        } 
    } 
}
