pipeline{
    agent any
    stages {
        stage('Run mortgage.py') {
            steps{
                sh '''
                python3 src/mortgage.py > mortgage_out.txt 
                '''
            }
        }
        stage('Run report.py') {
            steps{
                sh '''
                cd src
                python3 report.py > ../report_out.txt
                '''
            }
        }
    }
}
