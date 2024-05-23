pipeline {
    agent any

    stages {
        stage('Stage 1') {
            steps {
                // Your stage 1 steps here
                echo"Stage 1 is Running is ok"
            
            }
            
            post {
                success {
                    emailext (
                        subject: "PROJECT_NAME: Notifyer Stage 1 Completed Successfully",
                        body: ''' <html>
                            <body>
                                  <p>Build Status: ${BUILD_STATUS}</p>
                                  <p>Build Number: ${BUILD_NUMBER}</p>
                                  <p>Check the <a href="${BUILD_URL}">Console output</a>.</p>
                            </body>
                            </html>''',
                        to: "shubham.ssc100@gmail.com",
                        from:'jenkins@example.com',
                        replyTo:'jenkins@example.com',
                        mimeType:'text/html'
                    )
                }
                unstable {
                     emailext (
                        subject: "PROJECT_NAME: Notifyer Stage 1 Completed with some issue",
                        body: ''' <html>
                            <body>
                                  <p>Build Status: ${BUILD_STATUS}</p>
                                  <p>Build Number: ${BUILD_NUMBER}</p>
                                  <p>Check the <a href="${BUILD_URL}">Console output</a>.</p>
                            </body>
                            </html>''',
                        to: "shubham.ssc100@gmail.com",
                        from:'jenkins@example.com',
                        replyTo:'jenkins@example.com',
                        mimeType:'text/html'
                    )
                        
                }
                failure {
                     emailext (
                        subject: "PROJECT_NAME: Notifyer Stage 1 is Failed",
                        body: ''' <html>
                            <body>
                                  <p>Build Status: ${BUILD_STATUS}</p>
                                  <p>Build Number: ${BUILD_NUMBER}</p>
                                  <p>Check the <a href="${BUILD_URL}">Console output</a>.</p>
                            </body>
                            </html>''',
                        to: "shubham.ssc100@gmail.com",
                        from:'jenkins@example.com',
                        replyTo:'jenkins@example.com',
                        mimeType:'text/html'
                    )
        
            }
        }

    }

    }
}
