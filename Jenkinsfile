node('JDK8'){
    stage('sourcecode'){
        git branch: 'sprint1_develop', url: 'https://github.com/udaydevops2022/game-of-life.git'
    }
    stage('build the code'){
        sh 'mvn package'
    }
    stage('archiving and testresults'){
        junit '**/surefire-reports/*.xml'
        archiveArtifacts artifacts: '**/*.war', followSymlinks: false
    }

}