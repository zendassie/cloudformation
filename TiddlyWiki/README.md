# TiddlyWiki
A Cloudformation template to launch a TiddlyWiki site

## Template changes still todo:
1. Launch TiddlyWiki as a service
2. Map username and password input parameters to TiddlyWiki
3. Select existing Route53 domain and create a sub-domain (ex. from mydomain.com, create an alias wiki.mydomain.com)
4. Map this new domain name to the EC2 IP address

**Note:** I've excluded a load balancer simply because ELB's cost $. If this TiddlyWiki is for private use, an ELB is overkill.
