# TiddlyWiki
A CloudFormation template to launch a TiddlyWiki site

## How to use:
**Stack creation:**
1. In AWS => CloudFormation, select *Create Stack*
2. Select *Upload a template file* and upload the [TiddlyWiki.yaml](https://raw.githubusercontent.com/Juan007/cloudformation/master/TiddlyWiki/TiddlyWiki.yaml) file
2.1 Alternative paste this s3 [link](https://cf-templates-1coxzaw6pb2ki-eu-west-1.s3-eu-west-1.amazonaws.com/2019206Hl8-TiddlyWiki.yaml) in *Amazon S3 URL*
3. Click *Next*
4. Input the template parameters and click *Next* until you reach *Create Stack*

**Access your new wiki:**
1. Navigate to `yourwiki.yourdomain.com`
2. Type in your username and password
3. Enjoy!

> **Note:** I've excluded a load balancer simply because ELB's cost $. If this TiddlyWiki is for private use, an ELB is overkill.
