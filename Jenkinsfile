pipeline{
agent any
stages {
stage('Build Application') {
steps {
bat 'mvn clean install'
}
}
stage('Deploy CloudHubs') {
environment {
ANYPOINT_CREDENTIALS = credentials('b6c6e118-bc27-400a-b25a-bbe756affed6')
}
steps {
echo 'Deploying mule project due to the latest code commit…'
echo 'Deploying to the configured environment….'
bat 'mvn clean deploy -DmuleDeploy'
Dmule.app.name=mulesoft-ci-cd -Dusername= abrahamjo24 -Dpassword=aaAA@@1221'
}
}
}
}
