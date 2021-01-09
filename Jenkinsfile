pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                //
            }
        }
        stage('Test') {
            steps {
                //
            }
        }
        stage('Deploy') {
            steps {

            }
        }
        //From
        def remote = [:]
        remote.name = 'test'
        remote.host = 'test.domain.com'
        remote.user = 'root'
        remote.password = 'password'
        remote.allowAnyHosts = true
        stage('Remote SSH') {
            sshCommand remote: remote, command: "ls -lrt"
            sshCommand remote: remote, command: "for i in {1..5}; do echo -n \"Loop \$i \"; date ; sleep 1; done"
        }
    }
}
