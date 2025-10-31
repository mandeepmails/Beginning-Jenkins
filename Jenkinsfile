node('master || built-in') {
    stage('Fetch Source Code') {
        git 'https://github.com/mandeepmails/Beginning-Jenkins.git'// some block
    }
    dir('Lesson5') {
        printMessage('Running Pipeline')
        
        stage('Testing') {
            sh 'python test_functions.py'// some block
        }
        stage('Deployment') {
            if (env.BRANCH_NAME == 'main') {
                printMessage('Deploying the master branch')
            } else {
                printMessage('No Deploy configured for this branch')
            }
            
        }
        
        printMessage('Pipeline Complete')// some block
    }
    // some block
}

def printMessage(message) {
    echo "${message}"
}
