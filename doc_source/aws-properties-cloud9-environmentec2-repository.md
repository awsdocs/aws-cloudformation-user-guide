# AWS::Cloud9::EnvironmentEC2 Repository<a name="aws-properties-cloud9-environmentec2-repository"></a>

The `Repository` property type specifies an AWS CodeCommit source code repository to be cloned into an AWS Cloud9 development environment\.

## Syntax<a name="aws-properties-cloud9-environmentec2-repository-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloud9-environmentec2-repository-syntax.json"></a>

```
{
  "[PathComponent](#cfn-cloud9-environmentec2-repository-pathcomponent)" : String,
  "[RepositoryUrl](#cfn-cloud9-environmentec2-repository-repositoryurl)" : String
}
```

### YAML<a name="aws-properties-cloud9-environmentec2-repository-syntax.yaml"></a>

```
  [PathComponent](#cfn-cloud9-environmentec2-repository-pathcomponent): String
  [RepositoryUrl](#cfn-cloud9-environmentec2-repository-repositoryurl): String
```

## Properties<a name="aws-properties-cloud9-environmentec2-repository-properties"></a>

`PathComponent`  <a name="cfn-cloud9-environmentec2-repository-pathcomponent"></a>
The path within the development environment's default file system location to clone the AWS CodeCommit repository into\. For example, `/REPOSITORY_NAME` would clone the repository into the `/home/USER_NAME/environment/REPOSITORY_NAME` directory in the environment\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RepositoryUrl`  <a name="cfn-cloud9-environmentec2-repository-repositoryurl"></a>
The clone URL of the AWS CodeCommit repository to be cloned\. For example, for an AWS CodeCommit repository this might be `https://git-codecommit.us-east-2.amazonaws.com/v1/repos/REPOSITORY_NAME`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)