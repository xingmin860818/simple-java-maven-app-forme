pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /User/wecash/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
