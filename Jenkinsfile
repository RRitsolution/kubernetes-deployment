pipeline{

  agent any


  stages{

    stage('Checkout'){

      steps{

      git branch: 'main', url: 'https://github.com/RRitsolution/kubernetes-deployment.git'

      }
    }


    stage('Deployapps on eks'){

      steps{

        script{

          sh '''
           kubectl apply -f deployment.yaml
           kubectl apply -f service.yaml
          '''
        }
      }
    }
  }
}
           
      
