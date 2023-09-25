node ('ubuntu'){
	def app
	stage('Cloning Git') {
		checkout scm
	}
	stage('Build-and-Tag') {
		app = docker.build("dimeza/snake")

	}
	stage('Pull-image-server') {

		sh "compose down"
		sh "compose up -d"
	}
}
