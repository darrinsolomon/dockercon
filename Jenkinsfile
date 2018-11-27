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
<<<<<<< HEAD
      stage("Deploying sAPI") {
=======
      stage("Deploying Soap Proxy") {
>>>>>>> 0b91055d4c63344d6481edb14528768cd4b4e474
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
        steps {
<<<<<<< HEAD
 				  sh 'mvn -f sapi/pom.xml clean package deploy -Dmule.username=${ANYPOINT_CREDENTIALS_USR} -Dmule.password=${ANYPOINT_CREDENTIALS_PSW} -Dmule.URL=https://anypoint.mulesoft.com -DmuleDeploy'
      }
    }
      stage("Deploying pAPI") {
=======
 				  sh 'mvn -f retailpetstore/pom.xml clean package deploy -Dmule.username=${ANYPOINT_CREDENTIALS_USR} -Dmule.password=${ANYPOINT_CREDENTIALS_PSW} -Dmule.URL=https://anypoint.mulesoft.com -DmuleDeploy'
      }
    }
      stage("Updating and Re-Deploying pAPI") {
>>>>>>> 0b91055d4c63344d6481edb14528768cd4b4e474
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
        steps {
<<<<<<< HEAD
 				  sh 'mvn -f papi/pom.xml clean package deploy -Dmule.username=${ANYPOINT_CREDENTIALS_USR} -Dmule.password=${ANYPOINT_CREDENTIALS_PSW} -Dmule.URL=https://anypoint.mulesoft.com -DmuleDeploy'
      }
    }
      stage("Deploying eAPI") {
      environment {
        ANYPOINT_CREDENTIALS = credentials('anypoint.credentials')
      }
        steps {
          sh 'mvn -f eapi/pom.xml clean package deploy -Dmule.username=${ANYPOINT_CREDENTIALS_USR} -Dmule.password=${ANYPOINT_CREDENTIALS_PSW} -Dmule.URL=https://anypoint.mulesoft.com -DmuleDeploy'
      }
    }
    stage("Finishing Task") {
=======
 				  sh 'mvn -f papinew/pom.xml clean package deploy -Dmule.username=${ANYPOINT_CREDENTIALS_USR} -Dmule.password=${ANYPOINT_CREDENTIALS_PSW} -Dmule.URL=https://anypoint.mulesoft.com -DmuleDeploy'
      }
    }
      stage("Finishing Task") {
>>>>>>> 0b91055d4c63344d6481edb14528768cd4b4e474
      steps {
        echo "Deployment Completed on CH..."
      }
    }
  }
}
