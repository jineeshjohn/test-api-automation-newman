node("sbx") {
    checkout scm
    def buildContainer = docker.build("postman-newman-jenkins", "--no-cache .")
    stage("run newman tests") {
        buildContainer.inside {
          sh "npm run test"
        }
    }
}