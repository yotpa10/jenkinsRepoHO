pipeline {
    agent any
            stages {
                    stage('Get Latest from Git') {
                            steps {
                                    echo 'This is our first Jenkins pipeline'
                            }
                    }
                    
                    stage('Build') {
                            steps {
                                     withMaven(maven : 'maven_3_5_0') {
                                        echo 'This is our Build Stage'
                                    }
                            }
                    }
                
                    stage('Test') {
                            steps {
                                    withMaven(maven : 'maven_3_5_0') {
                                            echo 'This is our Testing Stage'
                                        }
                            }
                    }
                
                    stage('Deploy to Dev Box ') {
                            steps {
                                     input('Do you want to proceed?')
                            }
                    }
                    
                     stage('Deploy to QA Box ') {
                            steps {
                                     input('Do you want to proceed?')
                            }
                    }
                
                    stage('Deploy to Staging Box ') {
                            steps {
                                     input('Do you want to proceed?')
                            }
                    }
                
                    stage('Three') {
                        when {
                            not {
                                  branch "master"
                            }
                        }
                        steps {
                                echo "Hello"
                        }
                    }
                 }
            }
