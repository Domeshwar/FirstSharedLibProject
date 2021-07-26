pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '10'))
        disableConcurrentBuilds()
        timeout(time: 90, unit: 'MINUTES')
    }

    parameters {

        choice(name: 'Environment', choices:"PP\nPR", description: "Deployment Environment" )

	}
    stages {
	
  		stage("Declaring Environment Variables") {
		    
            steps {
                script {
                  
				  echo "I am cool"

                }
    }
	}
	}
}
