pipeline{
    agent any
    stages{
        stage("Upload to AWS"){
            steps{
                withAWS(credentials:'aws-static') {
                    s3Upload(file:'index.html', bucket:'mahmoud-project3', path:'index.html')

                }
                
            }
            
        }
    }
    
}