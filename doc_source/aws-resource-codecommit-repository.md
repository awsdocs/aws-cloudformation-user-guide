# AWS::CodeCommit::Repository<a name="aws-resource-codecommit-repository"></a>

Creates a new, empty repository\.

## Syntax<a name="aws-resource-codecommit-repository-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codecommit-repository-syntax.json"></a>

```
{
  "Type" : "AWS::CodeCommit::Repository",
  "Properties" : {
      "[Code](#cfn-codecommit-repository-code)" : Code,
      "[RepositoryDescription](#cfn-codecommit-repository-repositorydescription)" : String,
      "[RepositoryName](#cfn-codecommit-repository-repositoryname)" : String,
      "[Tags](#cfn-codecommit-repository-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Triggers](#cfn-codecommit-repository-triggers)" : [ RepositoryTrigger, ... ]
    }
}
```

### YAML<a name="aws-resource-codecommit-repository-syntax.yaml"></a>

```
Type: AWS::CodeCommit::Repository
Properties: 
  [Code](#cfn-codecommit-repository-code): 
    Code
  [RepositoryDescription](#cfn-codecommit-repository-repositorydescription): String
  [RepositoryName](#cfn-codecommit-repository-repositoryname): String
  [Tags](#cfn-codecommit-repository-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Triggers](#cfn-codecommit-repository-triggers): 
    - RepositoryTrigger
```

## Properties<a name="aws-resource-codecommit-repository-properties"></a>

`Code`  <a name="cfn-codecommit-repository-code"></a>
Information about code to be committed to a repository after it is created in an AWS CloudFormation stack\.  
You can only use this property to add code when creating a repository with a CloudFormation template at creation time\. This property cannot be used for updating code to an existing repository\.
*Required*: No  
*Type*: [Code](aws-properties-codecommit-repository-code.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RepositoryDescription`  <a name="cfn-codecommit-repository-repositorydescription"></a>
A comment or description about the new repository\.  
The description field for a repository accepts all HTML characters and all valid Unicode characters\. Applications that do not HTML\-encode the description and display it in a webpage can expose users to potentially malicious code\. Make sure that you HTML\-encode the description field in any application that uses this API to display the repository description on a webpage\.
*Required*: No  
*Type*: String  
*Maximum*: `1000`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RepositoryName`  <a name="cfn-codecommit-repository-repositoryname"></a>
The name of the new repository to be created\.  
The repository name must be unique across the calling AWS account\. Repository names are limited to 100 alphanumeric, dash, and underscore characters, and cannot include certain characters\. For more information about the limits on repository names, see [Limits](https://docs.aws.amazon.com/codecommit/latest/userguide/limits.html) in the *AWS CodeCommit User Guide*\. The suffix \.git is prohibited\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[\w\.-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-codecommit-repository-tags"></a>
One or more tag key\-value pairs to use when tagging this repository\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Triggers`  <a name="cfn-codecommit-repository-triggers"></a>
The JSON block of configuration information for each trigger\.  
*Required*: No  
*Type*: List of [RepositoryTrigger](aws-properties-codecommit-repository-repositorytrigger.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

## Return values<a name="aws-resource-codecommit-repository-return-values"></a>

### Ref<a name="aws-resource-codecommit-repository-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, `Ref` returns the repository ID\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-codecommit-repository-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-codecommit-repository-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
When you pass the logical ID of this resource, the function returns the Amazon Resource Name \(ARN\) of the repository\.

`CloneUrlHttp`  <a name="CloneUrlHttp-fn::getatt"></a>
When you pass the logical ID of this resource, the function returns the URL to use for cloning the repository over HTTPS\.

`CloneUrlSsh`  <a name="CloneUrlSsh-fn::getatt"></a>
When you pass the logical ID of this resource, the function returns the URL to use for cloning the repository over SSH\.

`Name`  <a name="Name-fn::getatt"></a>
When you pass the logical ID of this resource, the function returns the repository's name\.

## Examples<a name="aws-resource-codecommit-repository--examples"></a>

The following examples can help you create CodeCommit repositories using CloudFormation\.

### Example<a name="aws-resource-codecommit-repository--examples--Example"></a>

The following example creates a CodeCommit repository named *MyDemoRepo*\. The newly created repository is populated with code stored in an Amazon S3 bucket named *MySourceCodeBucket* and placed in a branch named *development*, which is the default branch for the repository\. 

#### JSON<a name="aws-resource-codecommit-repository--examples--Example--json"></a>

```
{
    "MyRepo": {
        "Type": "AWS::CodeCommit::Repository",
        "Properties": {
            "RepositoryName": "MyDemoRepo",
            "RepositoryDescription": "This is a repository for my project with code from MySourceCodeBucket.",
            "Code": {
                "BranchName": "development",
                "S3": {
                    "Bucket": "MySourceCodeBucket",
                    "Key": "MyKey",
                    "ObjectVersion": "1"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-codecommit-repository--examples--Example--yaml"></a>

```
MyRepo:
  Type: AWS::CodeCommit::Repository
  Properties:
    RepositoryName: MyDemoRepo
    RepositoryDescription: This is a repository for my project with code from MySourceCodeBucket.
    Code:
      BranchName: development
      S3: 
        Bucket: MySourceCodeBucket,
        Key: MyKey,
        ObjectVersion: 1
```

### Example<a name="aws-resource-codecommit-repository--examples--Example"></a>

The following example creates a CodeCommit repository with a trigger for all events in the main branch\. 

#### JSON<a name="aws-resource-codecommit-repository--examples--Example--json"></a>

```
{
    "MyRepo": {
        "Type": "AWS: : CodeCommit: : Repository",
        "Properties": {
            "RepositoryName": "MyRepoName",
            "RepositoryDescription": "a description",
            "Triggers": [
                {
                    "Name": "MainTrigger",
                    "CustomData": "Project ID 12345",
                    "DestinationArn": {
                        "Ref": "SNSarn"
                    },
                    "Branches": [
                        "main"
                    ],
                    "Events": [
                        "all"
                    ]
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-codecommit-repository--examples--Example--yaml"></a>

```
MyRepo:
  Type: AWS::CodeCommit::Repository
  Properties:
    RepositoryName: MyRepoName
    RepositoryDescription: a description
    Triggers:
    - Name: MainTrigger
      CustomData: Project ID 12345
      DestinationArn:
        Ref: SNSarn
      Branches:
      - main
      Events:
      - all
```