pipeline {
  agent {
    docker {
      image 'node:14' 
      }
     } 
     stages {
      stage('CLone repository') {
        steps{
          git branch: 'main', 
          url: 'https://github.com/Pranav120602/PES2UG20CS915_Jenkins.git'
          } 
        } 
        stage('Install dependencies') {
          steps {
            sh 'npm install' 
           } 
         } 
         stage('Build application') {
            steps {
              sh 'npm run build' 
              } 
           } 
           
           stage('Test application') {
            steps {
              sh 'npm test' 
              } 
           } 
           
           stage('Push Docker image') {
            steps {
              sh 'docker build -t pranavshankar/node:14 
              sh 'docker push pranavshankar/node:14 
              } 
            } 
         } 
     } 
