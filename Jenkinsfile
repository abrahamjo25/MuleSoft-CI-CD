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
ANYPOINT_CREDENTIALS = credentials('b90ebdcc-6d3b-401a-a3e2-88e6099f16b0')
}
steps {
echo 'Deploying mule project due to the latest code commit…'
echo 'Deploying to the configured environment….'
bat 'mvn clean deploy -DmuleDeploy -Dmule.app.name=mulesoft-ci-cd -Dusername= abrahamjo24 -Dpassword=aaAA1221'
}
}
}
}
