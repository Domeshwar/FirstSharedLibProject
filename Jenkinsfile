properties([
    parameters([
	      [
            $class: 'ChoiceParameter', 
            choiceType: 'PT_SINGLE_SELECT', 
            name: 'DataCenter', 
            randomName: 'datacenter-choice-parameter-102102304304506506', 
            script: [
                $class: 'ScriptlerScript', 
                scriptlerScriptId:'getdatacenters.groovy',
                fallbackScript: [ classpath: [], script: 'return ["N/A"]']
            ]
        ],

    ])
])

pipeline {
    agent any


    parameters {
        choice(name: 'ENVIRONMENT', choices: "${DataCenter}")
    }
    stages {
        stage("Run Tests") {
            steps {
                sh "echo SUCCESS on ${params.ENVIRONMENT}"
            }
        }
    }
}
