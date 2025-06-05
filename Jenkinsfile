pipeline{
	agent any
	tools{
		maven 'Maven'
	}
	stages{
		stage('Checkout'){
		steps{
		
			git branch:'master', url:'https://github.com/PrekshaVini/Maven5.git'
			}
	}
	stage('Build'){
		steps{
			sh 'mvn clean package'
		}
	}
	stage('Test'){
		steps{
			sh 'mvn test'
		}
	}
	stage('Run Application'){
		steps{
			sh 'java -jar target/Maven5-1.0-SNAPSHOT.jar'
		}
	}
}
post{
	success{
		echo 'Build success'
		}
	failure{
		echo 'Build failed'
		}
	}
}
		
