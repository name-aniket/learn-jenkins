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
			steps {
				echo "Region code: ${params.Region}"
			}		
		}
		stage('Deploy') {
			steps {
				echo "Count : ${params.Count}"
			}		
		}
	}
}
