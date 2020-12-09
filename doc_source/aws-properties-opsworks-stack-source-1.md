# AWS::OpsWorks::App Source<a name="aws-properties-opsworks-stack-source-1"></a>

Contains the information required to retrieve an app or cookbook from a repository\. For more information, see [Creating Apps](https://docs.aws.amazon.com/opsworks/latest/userguide/workingapps-creating.html) or [Custom Recipes and Cookbooks](https://docs.aws.amazon.com/opsworks/latest/userguide/workingcookbook.html)\.

## Syntax<a name="aws-properties-opsworks-stack-source-1-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opsworks-stack-source-1-syntax.json"></a>

```
{
  "[Password](#cfn-opsworks-custcookbooksource-pw)" : String,
  "[Revision](#cfn-opsworks-custcookbooksource-revision)" : String,
  "[SshKey](#cfn-opsworks-custcookbooksource-sshkey)" : String,
  "[Type](#cfn-opsworks-custcookbooksource-type)" : String,
  "[Url](#cfn-opsworks-custcookbooksource-url)" : String,
  "[Username](#cfn-opsworks-custcookbooksource-username)" : String
}
```

### YAML<a name="aws-properties-opsworks-stack-source-1-syntax.yaml"></a>

```
  [Password](#cfn-opsworks-custcookbooksource-pw): String
  [Revision](#cfn-opsworks-custcookbooksource-revision): String
  [SshKey](#cfn-opsworks-custcookbooksource-sshkey): String
  [Type](#cfn-opsworks-custcookbooksource-type): String
  [Url](#cfn-opsworks-custcookbooksource-url): String
  [Username](#cfn-opsworks-custcookbooksource-username): String
```

## Properties<a name="aws-properties-opsworks-stack-source-1-properties"></a>

`Password`  <a name="cfn-opsworks-custcookbooksource-pw"></a>
When included in a request, the parameter depends on the repository type\.  
+ For Amazon S3 bundles, set `Password` to the appropriate IAM secret access key\.
+ For HTTP bundles and Subversion repositories, set `Password` to the password\.
For more information on how to safely handle IAM credentials, see [https://docs.aws.amazon.com/general/latest/gr/aws-access-keys-best-practices.html](https://docs.aws.amazon.com/general/latest/gr/aws-access-keys-best-practices.html)\.  
In responses, AWS OpsWorks Stacks returns `*****FILTERED*****` instead of the actual value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Revision`  <a name="cfn-opsworks-custcookbooksource-revision"></a>
The application's version\. AWS OpsWorks Stacks enables you to easily deploy new versions of an application\. One of the simplest approaches is to have branches or revisions in your repository that represent different versions that can potentially be deployed\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SshKey`  <a name="cfn-opsworks-custcookbooksource-sshkey"></a>
In requests, the repository's SSH key\.  
In responses, AWS OpsWorks Stacks returns `*****FILTERED*****` instead of the actual value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-opsworks-custcookbooksource-type"></a>
The repository type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `archive | git | s3 | svn`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-opsworks-custcookbooksource-url"></a>
The source URL\. The following is an example of an Amazon S3 source URL: `https://s3.amazonaws.com/opsworks-demo-bucket/opsworks_cookbook_demo.tar.gz`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Username`  <a name="cfn-opsworks-custcookbooksource-username"></a>
This parameter depends on the repository type\.  
+ For Amazon S3 bundles, set `Username` to the appropriate IAM access key ID\.
+ For HTTP bundles, Git repositories, and Subversion repositories, set `Username` to the user name\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)