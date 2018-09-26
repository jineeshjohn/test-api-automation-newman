node {
    checkout scm
    def buildContainer = docker.build("postman-newman-jenkins", "--no-cache .")
    stage("run newman tests") {
        buildContainer.inside {
          sh "npm install"
          sh "npm run test"
        }
    }
}

// pipeline {
//     agent any
//     stages {
//         stage('Stage one') {
//             steps {
//                 script {
//                     echo "This is test message from stage one"
//                 }
//             }
//         }
//         stage('Stage two') {
//             steps {
//                 script {
//                    echo "This is test message from stage two"
//                 }
//             }
//         }
//     }
// }