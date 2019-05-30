node {
	   environment {
    registry = "kleku81/test_node"
    registryCredential = 'Docker_HUB'
  }
    checkout scm
    def customImage = docker.build("my-image:${env.BUILD_ID}")
    customImage.push()

    customImage.push('latest')
}
