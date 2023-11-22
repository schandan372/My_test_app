@Library('My_jenkins_shared_library') _
pipeline{
  agent any

  stages{
    stage('git Checkout'){
      steps{
        gitCheckout()
      }
    }
    stage('Build'){
      steps{
        build()
      }
    }
     stage('Sonar scan'){
      steps{
        sonarScan()
      }
    }
     stage('Artifact'){
      steps{
        jfrog()
      }
    }
     stage('Docker'){
      steps{
        dockerBuild()
      }
    }
     stage('Deploy'){
      steps{
        deploy()
      }
    }
  }
}
