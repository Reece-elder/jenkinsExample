// * Groovy Syntax
// ? Java based programming language

pipeline {
    agent any // What node you're using, don't bother editing

    environment {
        string = credentials('testString')
        gitCreds = credentials('gitCreds')
    }

    stages { // Collection of stages for this pipeline

        stage('helloWorld') { // What is the name of this stage

            steps { // What is done in this stage
                sh 'echo "helloWorld"' // Individual action of stage
                sh 'echo "helloWorld again"'
            }
        }

        stage('printCredential') {
            steps {
                sh 'echo $string'
                sh 'echo $gitCreds'
                sh 'echo $gitCreds_USR'
                sh 'echo $gitCreds_PW'
            }
        }

        stage('jenkinsActions') {
            steps {
                sh 'ls'
                sh 'pwd'
                // sh 'mkdir newDir'
                sh 'touch newestfile.txt'
                sh 'ls'
            }
        }

        stage('runScript'){
            steps {
                sh 'chmod +x test.sh'
                sh '. test.sh'
            }
        }
    }
}