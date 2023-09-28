# What is Nginx? 

Nginx [engine x] is server. In general terms, a server is a computing system into a network. What differentiate it from other server applications like Apache, among other characteristics, It could work as a reverse proxy server.

## What is a "reverse proxy" server?

* "reverse proxy" means the server handles incoming requests

* "proxy" means the server handles outgoing requests

A proxy server, whether or not reverse, It's a server application acting as intermediary between a request and its destination.

The, back into the question: What is Ngix?

* Among other common server features, It's an intermediary server application, placed between incoming request and its destination.

### More about Nginx

* Load balancing (distribute incoming requests to prevent from overloading, and also improve performace, etc.)
* Fault tolerance (gracefully errors handling, without disrupting the service)
* According to Netcraft, nginx served or proxied 20.86% busiest sites in August 2023. 
* Ran on many heavily loaded sites including Yandex, Mail.Ru, VK, and Rambler. And others like Dropbox, Netflix, Wordpress.com, FastMail.FM.

## Load balancing part?

Load balancing as feature provides the ability to distribute the usage, not by its own, It's commonly used in combination with Kubernets for orchrestation and Docker for the instances.

Docker creates the image of the Nginx application and creates the containers, then Kubernets manage the deployment of these containers and defines the entry points to reach Nginx.

## SSL Certificates

An SSL certificate is a digital certificate that authenticates a website's identity and enables an encrypted connection securing online transactions and keeping customer information private and secure. 

SSL stands for Secure Sockets Layer, a security protocol that creates an encrypted link between a web server and a web browser.

The SSL protocol ran into security issues, then TLS (Transport Layer Security) born as an evolution of that protocol. However, the initials SSL stuck around this process as SSL/TLS or just SSL certificates.

SSL certificates can be obtained directly from a Certificate Authority (CA). Certificate Authorities – sometimes also referred to as Certification Authorities – issue millions of SSL certificates each year.

### Let's Encrypt

Let’s Encrypt is a free, automated, and open certificate authority (CA). One of the biggest barriers til now has been the cost involved in getting a certificate. With Let’s Encrypt, this is no longer a concern because Let’s Encrypt makes SSL/TLS encryption freely available to everyone.

Certificates issued by Let’s Encrypt are trusted by most browsers today, including older browsers such as Internet Explorer on Windows XP SP3, and fully automates both issuing and renewing of certificates.

The process involves the Let’s Encrypt agent to generate SSL/TLS certificates for a registered domain name. Before issuing a certificate, Let’s Encrypt validates ownership of the domain. 

Then the Let’s Encrypt client, running on in the host, creates a temporary file (a token) with the required information in it. 

The Let’s Encrypt validation server then makes an HTTP request to retrieve the file and validates the token, which verifies that the DNS record for the domain resolves to the server running the Let’s Encrypt client. Finally, NGINX can be configured for automatic certificate renewals. 

# PoC: Nextjs, API, Nginx, Docker, and ECS/EC2

* https://developer.redis.com/create/docker/nodejs-nginx-redis/
* https://hkc7180.medium.com/nextjs-with-nginx-on-ec2-by-docker-compose-7558c838e0a4
* https://thoughtrealm.medium.com/deploying-a-next-js-app-with-nginx-using-docker-ca6a5bbb902e
* https://steveholgado.com/nginx-for-nextjs/
* https://blog.devops.dev/using-aws-cloud9-with-docker-to-deploy-a-nginx-static-website-7f19a13141ad

# SSL Certificates PoC

* https://www.nginx.com/blog/using-free-ssltls-certificates-from-lets-encrypt-with-nginx/
* https://phoenixnap.com/kb/letsencrypt-docker
* https://www.digitalocean.com/community/tutorials/how-to-secure-a-containerized-node-js-application-with-nginx-let-s-encrypt-and-docker-compose
* https://pentacent.medium.com/nginx-and-lets-encrypt-with-docker-in-less-than-5-minutes-b4b8a60d3a71
