# Bookstore web app

AWS Elastic Beanstalk - Deploy Java Web App on Tomcat with MySQL Database

Deploy a Java web app with MySQL database running on Apache Tomcat using Elastic Beanstalk web console

# 1.	Update project code – externalise datasource properties
JDBC_URL  System.getProperty(“JDBC_URL”)
JDBC_USERNAME  System.getProperty(“JDBC_USERNAME”)
JDBC_PASSWORD  System.getProperty(“JDBC_PASSWORD”)

# 2.	Package  & Test sample application on localhost
OK

# 3.	Create new application
AWS Elastic Beanstalk  Create application


# 4.	Configure Service access
Manually create a new role for EC2 instance
•	AWSElasticBeanstalkWebTier
•	AWSElasticBeanstalkWorkerTier
•	AWSElasticBeanstalkMulticontainerDocker


Manually create a new service role 
IAm/Roles/Create Role
Use case -> EC2
Search  awsElasticBeanstalk
•	Select -> 
•	AWSElasticBeanstalkWebTier
•	AWSElasticBeanstalkWorkerTier
•	AWSElasticBeanstalkMulticontainerDocker
Next
Name ->  elastic-beanstalk-ec2-role
Clic -> Create Role

Add new role to EC2 instance profile
# 5.	Configure database service

Enable RDS and choose MySQL
Enter app username and password

After RDS activating
Get schema name (DB name)
Get database host name (connection end point) and port number

# 6.	

# 7.	Deploy the application
Submit

# 8.	Add environment properties for database connection

Create environment property
Name: CATALINA_BASE_PORT
Value: 5000

JDBC_URL

JDBC_USERNAME

JDBC_PASSWORD
# 9.	Connect to remote MySQL server instance 


# 10. Test newly deployed application



