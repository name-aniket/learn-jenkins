pipeline {
	agent any

	parameters {
		string(name:'Cluster', defaultValue: 'cluster-1', description: 'Cluster name')
		string(name:'Region', defaultValue: 'region-1', description: 'Region code')
		string(name:'Count', defaultValue: '1', description: 'Number of tasks')
	}

	stages {

		stage('Build') {
			steps {
				echo "Cluster name: ${params.Cluster}"
			}		
		}

		stage('Test') {
				options {
					timeout(unit: 'SECONDS', time: 5)
				}
				
				steps {
					echo "Region code: ${params.Region}"					
					sleep 10					
				}
		}

		stage('Deploy') {
			
			steps {
				echo "Count : ${params.Count}"
			}		
		}
	}
	
	post {
		always {
			echo "Run regardless of the completion status of the Pipeline run."
		}
		changed {
			echo "Only run if the current Pipeline run has a different status."
		}
		failure {
			echo "Only run if the current Pipeline has a "failed" status."
		}
		success {
			echo "Only run if the current Pipeline has a "success" status."
		}
		unstable {
			echo "Only run if the current Pipeline has an "unstable" status."
		}
	}
}
