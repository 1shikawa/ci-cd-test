node{
 stage('Git Checkout'){
	git 'https://github.com/1shikawa/ci-cd-test'
 }

//  stage('Maven Package'){
// 	sh 'mvn clean package'
// 	sh 'mv target/myweb*.war target/myweb.war'
//  }

 stage('Build Docker Imager'){
   sh 'docker build -t 1shikawa/myweb:0.0.1 .'
 }

//  stage('Push to Docker Hub'){

// 	 withCredentials([string(credentialsId: 'github-pwd', variable: 'dockerHubPwd')]) {
//         sh "docker login -u kammana -p ${dockerHubPwd}"
//      }
// 	 sh 'docker push kammana/myweb:0.0.1'
//  }

//  stage('Remove Previous Container'){
// 	try{
// 		def dockerRm = 'docker rm -f myweb'
// 		sshagent(['docker-dev']) {
// 			sh "ssh -o StrictHostKeyChecking=no ec2-user@172.31.17.196 ${dockerRm}"
// 		}
// 	}catch(error){
// 		//  do nothing if there is an exception
// 	}
//  }

//  stage('Deploy to Dev Environment'){
//    def dockerRun = 'docker run -d -p 8080:8080 --name myweb kammana/myweb:0.0.1 '
//    sshagent(['docker-dev']) {
//     sh "ssh -o StrictHostKeyChecking=no ec2-user@172.31.17.196 ${dockerRun}"
//    }
//  }

}
