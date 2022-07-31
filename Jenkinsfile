pipeline{
    agent any{
        stages{
            stage('code fetch'){
                steps{
                sh "git credentialsId: '4668e75e-8fe0-4257-a93b-7a6d4e310b27', url: 'https://github.com/Srivani-Yelisetti/devopss.git"
                }
            }
            stage('compile'){
                steps{
                    sh "mvn compile"
                }
            }
            stage('codereview'){
                steps{
                sh "mvn pmd:pmd"
                }
            }
            stage('unittest'){
                steps{
                sh "mvn test"
                }
            }
            stage('package'){
                steps{
                sh "mvn package"
                }
            }
        }
    }
}
