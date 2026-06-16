pipeline{
agent any
tools{
maven 'Maven'
}
stages{
stage('checkout'){
steps{
git 'https://github.com/Disha-L12/rkd5.git'
}
}
stage('build'){
steps{
sh 'mvn clean package'
}
}
stage('archive'){
steps{
archiveArtifacts artifacts: 'target/*.war' ,fingerprint: true
}
}
stage('deploy'){
steps{
sh 'echo "deploy step here"'
}
}
}
post{
success{
echo 's'
}

failure{
echo 'f'}
}
}
