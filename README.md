
Creating Eureka server discovery and registering all created services (licensing service/ organization service) through Configuration server service (for Microservices concern separation).

The services (licensing and organization services) connected to PostgreSQL to a created database (database configuration in resources/config in configuration server through default and dev properties files).

1) Firstly, made it running in DEV mode trough Maven (all services running in localhost): Organization and Licensing services connected to PostgreSQL database and registered to Eureka server through configuration server configuration (filesystem with properties files and eureka-server.yml).

2) Then successfully tested the Spring cloud balancer library for client side load balancing with creating classes to test the communication between microservices (between Licensing service and organization service) using : DiscoveryClient/ RestTemplate/ Feign.

3) Finally, created Dockerfile for each services, created images (including postgreSQL running in a Docker container), then run all the containarized instances in Docker-compose for orchestration (created docker-compose.yml file) making the entire application successfully running through Docker containers.

PS: for the postgreSQL created also data.sql and init.sql to prepoluate the created database with some data.
