environments = 'lab\nstage\npro'

properties([
    parameters([
        [$class: 'CascadeChoiceParameter', 
            choiceType: 'PT_SINGLE_SELECT',
            description: 'Select a choice',
            name: 'choice1',
            referencedParameters: 'ENVIRONMENT',
            script: [$class: 'GroovyScript',
                fallbackScript: [
                    classpath: [], 
                    sandbox: true, 
                    script: 'return ["ERROR"]'
                ],
                script: [
                    classpath: [], 
                    sandbox: true, 
                    script: getenvtypesbydatacenter.groovy
                ]
            ]
        ]
    ])
])

pipeline {
    agent any


    parameters {
        choice(name: 'ENVIRONMENT', choices: "${environments}")
    }
    stages {
        stage("Run Tests") {
            steps {
                sh "echo SUCCESS on ${params.ENVIRONMENT}"
            }
        }
    }
}
