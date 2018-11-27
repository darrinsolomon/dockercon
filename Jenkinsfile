  pipeline {
  agent any
  
    tools{
      maven 'Maven 3.6.0'
    }
    stages {
    stage("Create Docker Container") {
      steps {
        echo "building container..."
      }
    }
    stage("Test maven") {
      steps {
          sh '''
            echo "Java_Home = $(java -version)"
            echo "Maven_Home = $(mvn -version)"
          '''
      }
    }
      stage("Deploying sAPI") {
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
        steps {
 				  sh 'mvn -f sapi/pom.xml clean package deploy -Dmule.username=${ANYPOINT_CREDENTIALS_USR} -Dmule.password=${ANYPOINT_CREDENTIALS_PSW} -Dmule.URL=https://anypoint.mulesoft.com -DmuleDeploy'
      }
    }
    stage("Finishing Task") {
      steps {
        echo "Deployment Completed on CH..."
      }
    }
  }
}
