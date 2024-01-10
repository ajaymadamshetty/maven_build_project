pipeline 
{
    agent any

    stages 
    {
        stage('Build') 
        {
            steps 
            {
                echo 'Build App in development ajay'
                sh 'terraform --version'
                sh 'terraform init'
                sh 'git --version'
                sh 'sudo mkdir /opt/madamshettyajay/heroman'
            }
        }
        stage('Test') 
        {
            steps 
            {
                echo 'Test App in dev'
            }
        }

        stage('Deploy') 
        {
            steps 
            {
                echo 'Deploy App in production'
            }
        }
    }

    post
    {

    	always
    	{
    		emailext body: 'Summary', subject: 'Pipeline Status', to: 'madamshettyajay@gmail.com'
    	}

    }
}
