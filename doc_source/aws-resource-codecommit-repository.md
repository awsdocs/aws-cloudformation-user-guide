# AWS::CodeCommit::Repository<a name="aws-resource-codecommit-repository"></a>

The `AWS::CodeCommit::Repository` resource creates an AWS CodeCommit repository that is hosted by Amazon Web Services\. For more information, see [Create an AWS CodeCommit Repository](http://docs.aws.amazon.com/codecommit/latest/userguide/how-to-create-repository.html) in the *AWS CodeCommit User Guide*\.

**Topics**
+ [Syntax](#aws-resource-codecommit-repository-syntax)
+ [Properties](#w3ab2c21c10d246b9)
+ [Return Values](#w3ab2c21c10d246c11)
+ [Example](#w3ab2c21c10d246c13)

## Syntax<a name="aws-resource-codecommit-repository-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codecommit-repository-syntax.json"></a>

```
{
  "Type" : "AWS::CodeCommit::Repository",
  "Properties" : {
    "[RepositoryDescription](#cfn-codecommit-repository-repositorydescription)" : String, required,
    "[RepositoryName](#cfn-codecommit-repository-repositoryname)" : String,
    "[Triggers](#cfn-codecommit-repository-triggers)" : [ [Trigger](aws-properties-codecommit-repository-triggers.md) ]
  }
}
```

### YAML<a name="aws-resource-codecommit-repository-syntax.yaml"></a>

```
Type: "AWS::CodeCommit::Repository"
Properties: 
  [RepositoryDescription](#cfn-codecommit-repository-repositorydescription): String
  [RepositoryName](#cfn-codecommit-repository-repositoryname): String
  [Triggers](#cfn-codecommit-repository-triggers):
  - [Trigger](aws-properties-codecommit-repository-triggers.md)
```

## Properties<a name="w3ab2c21c10d246b9"></a>

`RepositoryDescription`  <a name="cfn-codecommit-repository-repositorydescription"></a>
A description about the AWS CodeCommit repository\. For constraints, see the [CreateRepository](http://docs.aws.amazon.com/codecommit/latest/APIReference/API_CreateRepository.html) action in the *AWS CodeCommit API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RepositoryName`  <a name="cfn-codecommit-repository-repositoryname"></a>
A name for the AWS CodeCommit repository\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Triggers`  <a name="cfn-codecommit-repository-triggers"></a>
Defines the actions to take in response to events that occur in the repository\. For example, you can send email notifications when someone pushes to the repository\.  
*Required*: No  
*Type*: List of [AWS CodeCommit Repository Trigger](aws-properties-codecommit-repository-triggers.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d246c11"></a>

### Ref<a name="w3ab2c21c10d246c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the repository ID, such as `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d246c11b4"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the repository, such as `arn:aws:codecommit:us-east-1:123456789012:MyDemoRepo`\.

`CloneUrlHttp`  
The URL to use for cloning the repository over HTTPS, such as `https://codecommit.us-east-1.amazonaws.com/v1/repos/MyDemoRepo`\.

`CloneUrlSsh`  
The URL to use for cloning the repository over SSH, such as `ssh://git-codecommit.us-east-1.amazonaws.com/v1/repos//v1/repos/MyDemoRepo`\.

`Name`  
The name of the repository, such `MyDemoRepo`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="w3ab2c21c10d246c13"></a>

The following example creates an AWS CodeCommit repository with a trigger for all events in the `Master` branch\.

### JSON<a name="aws-resource-codecommit-repository-example.json"></a>

```
"MyRepo" : {
  "Type" : "AWS::CodeCommit::Repository",
  "Properties" : {
    "RepositoryName" : "MyRepoName",
    "RepositoryDescription" : "a description",
    "Triggers" : [
      {
        "Name" : "MasterTrigger",
        "CustomData" : "Project ID 12345",
        "DestinationArn" : { "Ref":"SNSarn" },
        "Branches" : ["Master"],
        "Events" : ["all"]
      }
    ]
  }
}
```

### YAML<a name="aws-resource-codecommit-repository-example.yaml"></a>

```
MyRepo:
  Type: AWS::CodeCommit::Repository
  Properties:
    RepositoryName: MyRepoName
    RepositoryDescription: a description
    Triggers:
    - Name: MasterTrigger
      CustomData: Project ID 12345
      DestinationArn:
        Ref: SNSarn
      Branches:
      - Master
      Events:
      - all
```