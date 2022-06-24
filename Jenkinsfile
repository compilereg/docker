pipeline {
    agent any

    stages {
       stage('Building') {
          steps {
             echo "Building "
          }
       }
       stage("Testing") {
          when{
            branch 'testing'
        }
        steps{
		      sh '''
                 echo "Testing .."
            '''
            }
       }

       stage("Deploy to main") {
          	when{
            branch 'main'
        }
        steps{
		      sh '''
                 echo "Deploying to main"
                 /usr/bin/rsync -avu --delete --exclude Jenkinsfile  --exclude .git*  --exclude composer --exclude vendor $(pwd)/ /apps/aast.edu/cms.aast.edu/
            '''
            }
       }

       stage("Deploy to test") {
          	when{
            branch 'testing'
        }
        steps{
		      sh '''
                 echo "Deploying to testing"
                  /usr/bin/rsync -avu --delete --exclude Jenkinsfile  --exclude .git* --exclude composer --exclude vendor $(pwd)/ /apps/aast.edu/cmstest.aast.edu/
            '''
            }
       }
    }
 }
    