pipeline
{
 agent any
 stages
 {
 	stage('Clean') 
 	{
            steps {
                sh "mvn clean -DdecryptionKey=${decryptionKey}"
            }
    }
    stage('Validate') 
 	{
            steps {
                sh "mvn validate -DdecryptionKey=${decryptionKey}"
            }
    }
    stage('Test') 
 	{
            steps {
                sh "mvn clean test -DdecryptionKey=${decryptionKey}"
            }
    }
 	stage('Build Application')
 	{
 		steps{
 				sh "mvn clean install -DskipMunitTests -DdecryptionKey=${decryptionKey}"
 			}
 	}
 	stage('Deploy To Artifactory')
 	{
 		steps{
 				sh "mvn deploy -DskipMunitTests -DdecryptionKey=${decryptionKey}"
 			}
 	}
 }
}