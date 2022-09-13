node{

stage('Clean Build') {
sh "./gradlew clean"
sh "pwd"

}
stage('Build release'){
sh './gradlew assembleRelease'
sh "pwd"
}
stage('Compile') {
archiveArtifacts artifacts: '**/*.apk', fingerprint: true,
onlyIfSuccessful: true
}
}
