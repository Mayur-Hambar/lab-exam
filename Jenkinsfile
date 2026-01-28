pipeline{
  agent any

  triggers {
    cron('* * * * *')
  }

  stages{ 
    stage('Checkout'){ steps{
      git branch: 'main', url: 'https://github.com/Mayur-Hambar/lab-exam/' }
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

    stage('Maven Run') {
            steps {
                sh 'java -cp target/simple-maven-1.0-SNAPSHOT.jar com.example.App'
            }
        }
  }
}
