# AWS Cloud9 EnvironmentEC2 Repository<a name="aws-properties-cloud9-environmentec2-repository"></a>

<a name="aws-properties-cloud9-environmentec2-repository-description"></a>The `Repository` property type specifies an AWS CodeCommit source code repository to be cloned into an AWS Cloud9 development environment\.

<a name="aws-properties-cloud9-environmentec2-repository-inheritance"></a> The `Repositories` property of the [AWS::Cloud9::EnvironmentEC2](aws-resource-cloud9-environmentec2.md) resource contains a list of `Repository` property types\.

## Syntax<a name="aws-properties-cloud9-environmentec2-repository-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloud9-environmentec2-repository-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-repository-pathcomponent)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-repository-repositoryurl)" : String
}
```

### YAML<a name="aws-properties-cloud9-environmentec2-repository-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-repository-pathcomponent): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-repository-repositoryurl): String
```

## Properties<a name="aws-properties-cloud9-environmentec2-repository-properties"></a>

`PathComponent`  
The path within the development environment's default filesystem location to clone the AWS CodeCommit repository into\. For example, `/repository-name` would clone the repository into the `/home/ec2-user/environment/repository-name` directory in the environment\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 

`RepositoryUrl`  
The clone URL of the AWS CodeCommit repository to be cloned\. For example, for an AWS CodeCommit repository this might be `https://git-codecommit.us-east-2.amazonaws.com/v1/repos/repository-name`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: No interruption 