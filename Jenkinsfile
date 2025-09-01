pipeline {
    agent any
    stages{
        stage('Checkout'){
            steps{
                git branch: 'master', url: "https://github.com/Divyansh6168/Jenkins-with-github.git"
            }
        }
        
        stage('Build'){
            steps{
                sh 'npm install'
                sh 'npm run build'
            }
        }
        
        stage('Test'){
            steps{
                sh 'npm test'
            }
        }
        
        stage('Deploy'){
            steps{
                sh '''
                    git config user.name "Divyansh6168"
                    git config user.email "divyanshrawat113@gmailcom"
                    git add -f build
                    git commit -m "Deploying build to Github pages"
                    git push origin `git subtree split --prefix build master`:gh-pages --force
                '''
            }
        }
    }
}
