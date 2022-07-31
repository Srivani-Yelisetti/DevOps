pipeline{
    agent any
    
        stages {
            stage ( 'compile' ) {
                steps {
                    git 'https://github.com/Srivani-Yelisetti/Devops.git'
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
            stage ( 'deploy' ) {
                steps {
                    sh 'docker build -t addressbook:1.0 .'
                    sh 'docker run -itd --name add -p 8188:8080 addressbook:1.0'
                }
            }
        }
}
            
