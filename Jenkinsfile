pipeline
{
    agent any
    stages
    {
        stage('ContinuousDownload_loans')
        {
            steps
            {
                git 'https://github.com/intelliqittrainings/maven.git'
            }
        }
        stage('ContinuousBuild_loans')
        {
            steps
            {
                sh 'mvn package'
            }
        }
	stage('ContinuousDeploy_loans')
        {
            steps
            {
                deploy adapters: [tomcat9(credentialsId: 'bfb67f1d-2f4e-430c-bb8d-30584116bd00', path: '', url: 'http://172.31.51.212:9090')], contextPath: 'test1', war: '**/*.war'
            }
        }


     
    }

    
}
