//pipeline {
//    agent any
//    stages {
//        stage('Build') {
//            steps {
//                echo 'Building Application'
//            }
//        }
//        stage('Test') {
//            steps {
//                echo 'Running Tests'
//            }
//        }
//    }
//}

//pipeline {
//   agent any

//   stages {

//stage('Build') {
//           steps {
//               sh 'npm install'
//           }
//       }

//       stage('Run') {
//           steps {
//               sh 'node index.js'
//           }
//       }

//   }
//}
pipeline {
    agent any

    stages {
        stage('Build Stage') {
            steps {
                sh 'npm install'
            }
        }

        stage('Deploy Stage') {
            steps {
                sh '''
                pm2 delete myapp || true
                pm2 start app.js --name myapp
                pm2 save
                '''
            }
        }
    }
}