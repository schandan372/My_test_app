@Library('My_jenkins_shared_library') _
pipeline{
  agent any

  stages{
    stage('git Checkout'){
      steps{
        script{
          gitCheckout()
      }
    }
    }
    stage('Build'){
      steps{
        script{
          build()
        }
      }
    }
     stage('Sonar scan'){
      steps{
        script{
          sonarScan()
        }
      }
    }
     stage('Artifact'){
      steps{
        script{
          jfrog()
        }
      }
    }
     stage('Docker'){
      steps{
        script{
          dockerBuild()
        }
      }
    }
     stage('Deploy'){
      steps{
        script{
          deploy()
        }
      }
    }
  }
}
