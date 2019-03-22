# Jenkins Shared Library
Shared Library sample for Jenkins


## Jenkins job example:
```
@Library('k8s-mgmt-library')_
    pipeline {
        agent any
        parameters {
            string(name: 'myInput', description: 'Some pipeline parameters')
        }
        stages {
            stage('Stage one') {
                steps {
                    script {
                        echo "First stage"
                        helloworld()
                    }
                }
            }
            stage('Stage two') {
                steps {
                    script {
                        echo "Second stage"
                    }
                }
            }
        }
    }
```
