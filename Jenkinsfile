node {

stage('SCM'){
 git 'https://github.com/Hiennguyenalice/test_projet_jenkins'
}

stage('Compile'){
def mvnHome = tool name: 'maven-3' , type: 'maven'
sh "${mvnHome}/bin/mvn package"
}

stage('SonarQube') {
  def mvnHome = tool name: 'maven-3' , type: 'maven'
  sh "${mvnHome}/bin/mvn sonar:sonar -Dsonar.host.url=http://192.168.1.64:9000"
    }
}
