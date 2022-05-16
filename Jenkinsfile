node('JDK8'){
    stage('SourceCode'){
        //get the code from gitrepo on the branch sptin1_develop
        git branch: 'sprin1_develop', url: 'https://github.com/udaydevops2022/game-of-life.git'
    }
    stage('Build the Code'){
        //get the build the code
        sh 'mvn package'
    }
    stage('archiving and test results'){
        //
        junit '**/surefire-reports/*.xml'
        archiveArtifacts artifacts: '**/*.war', followSymlinks: false
    }
}
