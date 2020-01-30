
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
	    MYSQL_DATABASE: wordpress
	    MYSQL_USER: interviewuser
	    MYSQL_PASSWORD: interv!3wpassw0rd
	    MYSQL_RANDOM_ROOT_PASSWORD: yes

Both services must be independent pods.

We are going to use a Centos instance 64.227.88.210 to perform the deployment.

## Items to complete:

 1. Create the Kubernetes configuration files to deploy WordPress and MySQL and commit them to the root of this repo.
 2. Pull this repo in 64.227.88.210 and execute the commands to deploy the application.

### Extra item:

 - Design the strategy to implement Zero Down Time when we upgrade MySQL from 5.7 to latest.

## References:

 - [MySQL Image info from docker hub](https://hub.docker.com/_/mysql?tab=description)
 - [WordPress Image info from docker hub](https://hub.docker.com/_/wordpress)

