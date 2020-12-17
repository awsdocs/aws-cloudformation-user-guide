# Microsoft Windows Amazon Machine Images \(AMIs\) and AWS CloudFormation templates<a name="cfn-windows-stacks-amis-and-templates"></a>

With AWS CloudFormation, you can create Microsoft Windows stacks for running Windows server instances\. A number of pre\-configured templates are available to launch directly from the [AWS CloudFormation sample templates page](http://aws.amazon.com/cloudformation/aws-cloudformation-templates/), such as the following templates:
+ [Windows\_Single\_Server\_SharePoint\_Foundation\.template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/Windows_Single_Server_SharePoint_Foundation.template) \- SharePoint® Foundation 2010 running on Microsoft Windows Server® 2008 R2
+ [Windows\_Single\_Server\_Active\_Directory\.template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/Windows_Single_Server_Active_Directory.template) \- Create a single server installation of Active Directory running on Microsoft Windows Server® 2008 R2\.
+ [Windows\_Roles\_And\_Features\.template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/Windows_Roles_And_Features.template) \- Create a single server specifying server roles running on Microsoft Windows Server® 2008 R2\.
+ [ElasticBeanstalk\_Windows\_Sample\.template](https://s3.amazonaws.com/cloudformation-templates-us-east-1/ElasticBeanstalk_Windows_Sample.template) \- Launch an AWS Elastic Beanstalk sample application on Windows Server 2008 R2 running IIS 7\.5\.

**Note**  
Microsoft, Windows Server, and SharePoint are trademarks of the Microsoft group of companies\.

Although these stacks are already configured, you can use any EC2 Windows AMI as the basis of an AWS CloudFormation Windows stack\. 