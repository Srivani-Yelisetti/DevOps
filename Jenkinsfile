pipeline{
    agent any
    
        stages {
            stage ( 'compile' ) {
                steps {
                    git 'https://github.com/Srivani-Yelisetti/Devops.git'
                    sh "mvn compile"
                }
            }
            /*stage ( 'codereview' ){
                steps {
                sh "mvn pmd:pmd"
                }
            }*/
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
            stage ( 'deploy' ) {
                steps {
                    sh 'docker build -t addressbook:2.0 .'
                    sh 'docker run -itd --name add1 -p 8189:8080 addressbook:2.0'
                }
            }
        }
}
            
