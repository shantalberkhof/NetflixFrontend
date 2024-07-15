pipeline {
    agent any
    
    triggers {
        githubPush()
    }

    stages {
        stage('Build app container') {
            steps {
                sh '''
                    # Navigate to the working directory
                    cd ~/NetflixFrontend

                    # List the files in the pipeline workdir
                    ls 

                    # Build the Docker image
                    docker build -t netflix-front .

                    # run the container to verify it's working
                    # docker run -d -p 80:80 netflix-front
                '''
            }
        }
    }
}
