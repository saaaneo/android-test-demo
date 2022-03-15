node {
   def gdlHome
    stage('pull repo') { 
        git branch: 'master', url: 'https://github.com/saaaneo/android-test-demo.git'
        gdlHome = tool 'G7'
    }
    stage('Build') {
    withEnv(["GDL_HOME=$gdlHome"]) {
		sh '"$GDL_HOME/bin/gradle" build'
	    }
    }
}
