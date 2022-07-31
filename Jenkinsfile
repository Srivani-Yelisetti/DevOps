pipeline{
    agent any
    
        stages {
            stage ( 'compile' ) {
                steps {
                    sh 'https://github.com/Srivani-Yelisetti/Devops.git'
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
