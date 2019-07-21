# TiddlyWiki
A CloudFormation template to launch a TiddlyWiki site

## How to use:
**Stack creation:**
1. In AWS => CloudFormation, select *Create Stack*
2. Select *Upload a template file* and upload the [TiddlyWiki.yaml](https://raw.githubusercontent.com/Juan007/cloudformation/master/TiddlyWiki/TiddlyWiki.yaml) file
3. Click *Next*
4. Input the template parameters and click *Next* until you reach *Create Stack*

**Initial setup:**
1. After the stack has successfully been created, navigate to your newly created EC2 instance, sopy the URL and SSH in using the pre-shared key that you attached during stack creation.
2. Once logged in, execute:
```
sudo tiddlywiki <YourWikiName> --init server
sudo tiddlywiki <YourWikiName> --listen host=0.0.0.0 port=8080 username=<YourUsername> password=<YourPassword>
```

**Access your new wiki:**
1. Navigate to `<Your-EC2-Server-IP:8080>`
2. Type in your username and password
3. Enjoy!

## Template changes still todo:
1. Launch TiddlyWiki as a service
2. Map username and password input parameters to TiddlyWiki
3. Select existing Route53 domain and create a sub-domain (ex. from mydomain.com, create an alias wiki.mydomain.com)
4. Map this new domain name to the EC2 IP address
5. Create and optional parameter that maps to an existing S3 bucket. This will then backup the wiki and restore from there if there's already data.

Once the above is done, the **Initial Setup** will no longer be needed and you will no longer need to have your terminal open in order to borwse to your wiki.

> **Note:** I've excluded a load balancer simply because ELB's cost $. If this TiddlyWiki is for private use, an ELB is overkill.
