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

    stage('Prometheous & Grafana setup//Helm repository add'){

      steps{

        script{
          sh '''

          helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
          helm repo add grafana https://grafana.github.io/helm-charts
          helm repo update

          '''

          
  }
}
           
      
