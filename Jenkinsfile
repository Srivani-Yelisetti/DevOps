pipeline{
    agent any
    
        stages {
            stage ( 'code fetch' ) {
                steps {
                sh 'https://github.com/Srivani-Yelisetti/Devops.git'
                }
            }
            stage ( 'compile' ) {
                steps {
                    sh "mvn compile"
                }
            }
            stage ( 'codereview' ){
                steps {
                sh "mvn pmd:pmd"
                }
            }
            stage ( 'unittest' ){
                steps {
                sh "mvn test"
                }
            }
            stage ( 'package' ) {
                steps {
                sh "mvn package"
                }
            }
        }
}
