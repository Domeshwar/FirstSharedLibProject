pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '10'))
        disableConcurrentBuilds()
        timeout(time: 90, unit: 'MINUTES')
    }

 parameters {
         activeChoiceParam('choice1') {
                      description('select your choice')
                      choiceType('RADIO')
                      groovyScript {
                          script('return["aaa","bbb"]')
                          fallbackScript('return ["error"]')
                      }
        }
        activeChoiceReactiveParam('choice2') {
                      description('select your choice')
                      choiceType('RADIO')
                      groovyScript {
                          script(' if(choice1.equals("aaa")) { return ["a", "b"] } else {return ["aaaaaa","fffffff"] } ')
                          fallbackScript('return ["error"]')
                      }
                      referencedParameter('choice1')
        }
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
