
# Interview DEVOPS

For this exercise we are going to deploy WordPress with a MySQL Database in a Kubernetes cluster.

**Note:** The passwords will be provided during the interview.

The information about the WordPress container:

    image: wordpress:latest
    ports: 8080:80
    evironment variables:
	    WORDPRESS_DB_HOST: my_db
	    WORDPRESS_DB_USER: interviewuser
	    WORDPRESS_DB_PASSWORD: interv!3wpassw0rd
	    WORDPRESS_DB_NAME: wordpress
    
  For MySQL:
  
    image: mysql:5.7
    evironment variables:
	    MYSQL_DATABASE: my_db
	    MYSQL_USER: interviewuser
	    MYSQL_PASSWORD: interv!3wpassw0rd
	    MYSQL_RANDOM_ROOT_PASSWORD: yes

Both services must be independent pods.

We are going to use a Jenkins instance ([http://157.245.224.231:8080/job/interview_test_job/](http://157.245.224.231:8080/job/interview_test_job/)) for the deployment.

## Items to complete:

 1. Create configuration files to deploy WordPress and MySQL and commit them to the root of this repo.
 2. Configure the previous Jenkins job to deploy them into the cluster.
 3. Login into the Jenkins machine as root and verify the cluster is up and running using a kubectl command.

### Extra item:

 - Design the strategy to implement Zero Down Time when we upgrade MySQL from 5.7 to latest.

## References:

 - [MySQL Image info from docker hub](https://hub.docker.com/_/mysql?tab=description)
 - [WordPress Image info from docker hub](https://hub.docker.com/_/wordpress)
 - [Kubernetes Plugin in Jenkins](https://github.com/jenkinsci/kubernetes-plugin)

