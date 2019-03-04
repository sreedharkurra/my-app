  node{
   stage('SCM Checkout'){
     git 'https://github.com/sreedharkurra/my-app.git'
   }
   stage('Compile-Package'){
    
      def mvnHome =  tool name: 'maven', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
      mail bcc: '', body: '''Hi Welcome to jenkins email alerts
      Thanks
      Hari''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'kurra.sreedhar@gmail.com'
   }
  }


