node {
    def mavenHome = tool name: "maven3.8.4"
    stage ('checkoutcode'){
        git branch: 'main', credentialsId: 'github', url: 'https://github.com/divyeshbhalekar/first-pipeline.git'
    }
    stage ('build'){
        sh "${mavenHome}/bin/mvn clean package"
    }
    /* stage ('deplo-appln'){
        sshagent(['55a8a4eb-bb93-4618-a4fb-c91fffeeccc9']) {
            sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/first-pipeline/webapp/target/webapp.war ec2-user@34.239.108.72:/home/ec2-user/apache-tomcat-9.0.58/webapps/"
            
}
    } */
}
