pipeline{
    agent {
	label 'k8s'
    }

    stages{
        stage('Build'){
            steps{
                sh "mvn clean package"
            }
        }
        stage('Archive'){
            steps{
                archiveArtifacts artifacts: '**/target/*.jar' 
            }
        }
    }
}
