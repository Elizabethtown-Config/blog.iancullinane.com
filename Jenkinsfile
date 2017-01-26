git_creds = 'e6a36c15-1342-4105-9ef8-896857a5781c'
git_url = 'git@github.com:eignhpants/'
project = 'deployment'
git_url = "${git_url}${project}.git"


node(NODE_LABEL){

    stage "Checkout Deployment"
    git branch: "master", credentialsId: git_creds, url: git_url

    stage "Deploy Blog"
    sh "ls -la"
    sh "docker-compose down"
    sh "docker-compose pull"
    sh "docker-compose -f blog.iancullinane.com.yml up -d"

}
