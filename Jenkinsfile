pipeline{
  agent any

  trigger{
    build('* * * * *')
  }

  stages{
    stage('Checkout'){
      git branch: 'main', url: 'https://github.com/Mayur-Hambar/lab-exam/'
    }

    stage('Maven Test'){
      steps{
        sh 'mvn test'
      }
    }

    stage('Maven Build'){
      steps{
        sh 'mvn clean package'
      }
    }
  }
}
