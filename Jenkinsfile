pipeline {
agent any
stages {
stage ('
Build
') {
steps {
sh '
mvn clean package
'
}
}
stage ('
SonarQube Analyses
') {
steps {
withSonarQubeEnv('
sonar6
') {
sh '
mvn sonar:sonar -Dsonar.host.url=
http://10.0.2.100:9000 -Dsonar.login=admin -Dsonar.password=admin123
'
}
}
}
}
}
