pipeline {
    agent any
    
    options{
        timestamps()
        ansiColor("xterm")
    }
    stages {
        stage('EB create'){
            steps {
                 withAWS(credentials: 'aws-access-key', region: 'eu-west-1') {
                    dir("eb") {
                        sh 'eb create cmg-elastic'
                    }
                 }
            }
        }
    }
}
