node {
  stage('SCM') 
    {
        echo 'Gathering code from version control'
        git branch: '${branch}', url: 'https://github.com/sheshankpriyadarshi/jenkins.git'
    }
    stage('Build') 
    {
      try{
        bat 'dotnet --version' 
        bat 'dotnet build ConsoleApp1'
        echo 'Building new feature...'
      }
      catch(e)
      {
        echo 'something is not right'
        echo e.toString();
        currentBuild.result = "FAILURE"
      }
      finally
      {
        //cleanup
      }
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