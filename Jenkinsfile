pipeline{
    agent any
    stages{
        stage("Lint HTML"){
            sh 'tidy -q -e *.html'
        }
        stage("Upload to AWS"){
            steps{

                withAWS(credentials:'aws-static') {
                    s3Upload(file:'index.html', bucket:'mahmoud-project3', path:'index.html')

                }
                
            }
            
        }
    }
    
}