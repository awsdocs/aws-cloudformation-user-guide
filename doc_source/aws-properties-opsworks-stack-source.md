# AWS OpsWorks Source Type<a name="aws-properties-opsworks-stack-source"></a>

Describes the information required to retrieve a cookbook or app from a repository for the [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md) or [AWS::OpsWorks::App](aws-resource-opsworks-app.md) resource types\.

For more information and valid values, see [Source](http://docs.aws.amazon.com/opsworks/latest/APIReference/API_Source.html) in the *AWS OpsWorks Stacks API Reference*\.

## Syntax<a name="w3ab2c21c14e1589b7"></a>

### JSON<a name="aws-properties-opsworks-stack-source-syntax.json"></a>

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

### YAML<a name="aws-properties-opsworks-stack-source-syntax.yaml"></a>

```
[Password](#cfn-opsworks-custcookbooksource-pw): String
[Revision](#cfn-opsworks-custcookbooksource-revision): String
[SshKey](#cfn-opsworks-custcookbooksource-sshkey): String
[Type](#cfn-opsworks-custcookbooksource-type): String
[Url](#cfn-opsworks-custcookbooksource-url): String
[Username](#cfn-opsworks-custcookbooksource-username): String
```

## Properties<a name="w3ab2c21c14e1589b9"></a>

`Password`  <a name="cfn-opsworks-custcookbooksource-pw"></a>
This parameter depends on the repository type\. For Amazon S3 bundles, set `Password` to the appropriate IAM secret access key\. For HTTP bundles, Git repositories, and Subversion repositories, set `Password` to the appropriate password\.  
*Required*: No  
*Type*: String

`Revision`  <a name="cfn-opsworks-custcookbooksource-revision"></a>
The application's version\. With AWS OpsWorks, you can deploy new versions of an application\. One of the simplest approaches is to have branches or revisions in your repository that represent different versions that can potentially be deployed\.  
*Required*: No  
*Type*: String

`SshKey`  <a name="cfn-opsworks-custcookbooksource-sshkey"></a>
The repository's SSH key\. For more information, see [Using Git Repository SSH Keys](http://docs.aws.amazon.com/opsworks/latest/userguide/workingapps-deploykeys.html) in the *AWS OpsWorks User Guide*\.  
To pass in an SSH key as a parameter, see the following example:  

```
"Parameters" : {
  "GitSSHKey" : {
    "Description" : "Change SSH key newlines to commas.",
    "Type" : "CommaDelimitedList",
    "NoEcho" : "true"
  },

...
   
  "CustomCookbooksSource": {
    "Revision" : { "Ref": "GitRevision"},
    "SshKey" : { "Fn::Join" : [ "\n", { "Ref": "GitSSHKey"} ] },
    "Type": "git",
    "Url": { "Ref": "GitURL"}
  }

...
```
*Required*: No  
*Type*: String

`Type`  <a name="cfn-opsworks-custcookbooksource-type"></a>
The repository type\.  
*Required*: No  
*Type*: String

`Url`  <a name="cfn-opsworks-custcookbooksource-url"></a>
The source URL\.  
*Required*: No  
*Type*: String

`Username`  <a name="cfn-opsworks-custcookbooksource-username"></a>
This parameter depends on the repository type\. For Amazon S3 bundles, set `Username` to the appropriate IAM access key ID\. For HTTP bundles, Git repositories, and Subversion repositories, set `Username` to the appropriate user name\.  
*Required*: No  
*Type*: String