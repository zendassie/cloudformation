# TiddlyWiki
A CloudFormation template to launch a TiddlyWiki site

## How to use:
**Prerequisite:**
1. An [AWS account](https://aws.amazon.com/#)
1. A valid [EC2 Key Pair](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html)
1. A valid [Route53 Domain](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Welcome.html)
> Note: If you don't want to register a domain, simply delete the following sections: Under *Parameters*, delete the *Route53HostedZone* and *UrlName* sections. Under *Resources*, delete the *Url* section. Then once your stack has launched, head over to your EC2 instance and use the *AWS Public DNS* or *IPv4 Public IP* to navigate to your wiki.

**Stack creation:**
1. In AWS => [CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/GettingStarted.html), select *Create Stack*
2. Select *Upload a template file* and upload the [TiddlyWiki.yaml](https://raw.githubusercontent.com/Juan007/cloudformation/master/TiddlyWiki/TiddlyWiki.yaml) file
> Alternatively paste this s3 [link](https://cf-templates-1coxzaw6pb2ki-eu-west-1.s3-eu-west-1.amazonaws.com/2019206Hl8-TiddlyWiki.yaml) in *Amazon S3 URL*
3. Click *Next*
4. Input the template parameters and click *Next* until you reach *Create Stack*

**Access your new wiki:**
1. Navigate to `yourwiki.yourdomain.com`
1. Type in your username and password
1. Enjoy!

> **Note:** I've excluded a load balancer simply because ELB's cost $. If this TiddlyWiki is for private use, an ELB is overkill.
