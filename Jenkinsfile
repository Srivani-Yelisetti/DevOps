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
                sh 'https://github.com/Srivani-Yelisetti/Devops.git'
                sh "mvn pmd:pmd"
                }
            }
            stage ( 'unittest' ){
                steps {
                    sh 'https://github.com/Srivani-Yelisetti/Devops.git'
                    sh "mvn test"
                }
            }
            stage ( 'package' ) {
                steps {
                    sh 'https://github.com/Srivani-Yelisetti/Devops.git'
                    sh "mvn package"
                }
            }
        }
}
