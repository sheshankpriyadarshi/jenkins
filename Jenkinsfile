node {
  stage('SCM') 
    {
        echo 'Gathering code from version control'
        git branch: '${branch}', url: 'https://github.com/sheshankpriyadarshi/jenkins.git'
    }
    stage('Build') 
    {
        sh 'dotnet --version' 
        sh 'dotnet build ConsoleApp1'
        echo 'Building new feature...'
    }
      stage('Test') 
    {
        echo 'Testing...'
    }
      stage('Deploy') 
    {
        echo 'Deploying...'
    }
}