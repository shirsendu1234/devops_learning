pipeline {
    agent any
            stages {
                    stage('git-checkout') {
							steps {
							// One or more steps need to be included within the steps block.
								echo "building the project"
								git branch: 'main', credentialsId: '5f371c98-c212-486a-8c0e-ad8b07bb9071', url: 'https://github.com/Smitha1991/pipeline_script.git'
								}
						}

                
                    stage('Build') {
                            steps {
                                    echo "building the project"
                                    echo pwd()
                                    echo "${env.WORKSPACE}"
                                    sh "chmod +x -R ${env.WORKSPACE}/Build.sh"
                                    sh './Build.sh'
                            }
                    }
                    
                 }
            }
