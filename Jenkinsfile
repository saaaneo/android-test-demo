node {
    def gdlHome
    stage('Preparation') { 
        git 'https://github.com/saaaneo/android-test-demo.git'
        gdlHome = tool 'G7'
    }
    stage('Build') {
        // Run the gradle build
        withEnv(["GDL_HOME=$gdlHome"]) {
            if (isUnix()) {
                sh '"$GDL_HOME/bin/gradle" clean build'
            } else {
                bat(/"%GDL_HOME%\bin\gradle" clean build)
            }
        }
    }
}
