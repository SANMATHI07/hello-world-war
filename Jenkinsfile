pipeline { 
    agent {label 'slave7'}
    stages { 
        stage ('checkout') { 
            steps {
                sh "pwd"
                sh "rm -rf hello-world-war"
                sh "git clone https://github.com/praveen1895/hello-world-war.git"
            }
        }
        stage ('build') { 
             steps {
                sh "ls"
                sh "cd hello-world-war"
                sh "mvn clean package"
             }
        }
        stage ('deploy') { 
             steps {
              sh "cp /home/slave7/workspace/tomtest/target/hello-world-war-1.0.0.war /opt/tomcat/webapps" 
             }
        }
        stage ('QA') { 
             steps {
                echo "QA"
             }
        }
        stage ('Monitor') { 
             steps {
                echo "Monitor"
             }
        }
 
    }           
 }
