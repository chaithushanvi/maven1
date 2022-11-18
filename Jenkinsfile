pipeline
{
    agent any
    stages
    {
        stage('ContinuousDownload_scm')
        {
            steps
            {
                git 'https://github.com/intelliqittrainings/maven.git'
            }
        }
        stage('ContinuousBuild_scm')
        {
            steps
            {
                sh 'mvn package'
            }
        }

     
    }

    
}
