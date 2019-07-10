node('master'){
    
    stage('pull_code_gitubh')
    {
        git 'https://github.com/devopsloves/axis-demo.git'
    }
    
    stage('maven_clean')
    {
       tool name: 'maven', type: 'maven' 
        sh 'mvn clean'
    }
    stage('maven_compile'){
        
        sh 'mvn compile'
    }
    
    stage('maven_test')
    {
        sh 'mvn test'
    }
    stage('pacakge'){
        
        sh 'mvn package'
    }
    
    stage('deploy_war')
    {
        sh 'cp target/axis.war /opt/apache-tomcat-8.5.42/webapps/'
    }
    
}
