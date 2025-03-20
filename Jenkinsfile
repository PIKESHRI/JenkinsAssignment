pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building Code'
                sh ''' 
                mkdir -p build
                touch build/index.html
                echo "This is the index file" >> build/index.html
                cat build/index.html

                '''
            }
        }
        stage('Test'){
            steps{
                sh ''' 
                      if [-f build/index.html]; then
                       echo "index.html exist"
                      else
                       echo "index.html doesn't exist"
                   '''
                echo 'Test Executed'
            }
        }
    }
}