pipeline{
agent any
tools{
maven 'Maven'
}
stages{
stage('Checkout'){
steps{
git branch:'Master',url:'https://github.com/sinchanam12/SinchanaMaven.git'
}
}
stage('Build'){
steps{
sh'mvn clean package'
}
}
stage('Test'){
steps{
sh'mvn test'
}
}
stage('Run Application'){
steps{
sh'java -jar target/SinchanaMaven-1.0-SNAPSHOT.jar'a
}
}
}
post{
success{
echo'Build and deployment successful'
}
failure{
echo'build failed'
}
}
}
