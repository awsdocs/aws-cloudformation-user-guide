# AWS::CodeGuruReviewer::RepositoryAssociation<a name="aws-resource-codegurureviewer-repositoryassociation"></a>

This resource configures how Amazon CodeGuru Reviewer retrieves the source code to be reviewed\. You can use an AWS CloudFormation template to create an association with the following repository types:
+ AWS CodeCommit \- For more information, see [Create an AWS CodeCommit repository association](https://docs.aws.amazon.com/codeguru/latest/reviewer-ug/create-codecommit-association.html) in the *Amazon CodeGuru Reviewer User Guide*\. 
+ Bitbucket \- For more information, see [Create a Bitbucket repository association](https://docs.aws.amazon.com/codeguru/latest/reviewer-ug/create-bitbucket-association.html) in the *Amazon CodeGuru Reviewer User Guide*\. 
+ GitHub Enterprise Server \- For more information, see [Create a GitHub Enterprise Server repository association](https://docs.aws.amazon.com/codeguru/latest/reviewer-ug/create-github-enterprise-association.html) in the *Amazon CodeGuru Reviewer User Guide*\. 

**Note**  
 You cannot use a CloudFormation template to create an association with a GitHub repository\. 

## Syntax<a name="aws-resource-codegurureviewer-repositoryassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codegurureviewer-repositoryassociation-syntax.json"></a>

```
{
  "Type" : "AWS::CodeGuruReviewer::RepositoryAssociation",
  "Properties" : {
      "[ConnectionArn](#cfn-codegurureviewer-repositoryassociation-connectionarn)" : String,
      "[Name](#cfn-codegurureviewer-repositoryassociation-name)" : String,
      "[Owner](#cfn-codegurureviewer-repositoryassociation-owner)" : String,
      "[Tags](#cfn-codegurureviewer-repositoryassociation-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-codegurureviewer-repositoryassociation-type)" : String
    }
}
```

### YAML<a name="aws-resource-codegurureviewer-repositoryassociation-syntax.yaml"></a>

```
Type: AWS::CodeGuruReviewer::RepositoryAssociation
Properties: 
  [ConnectionArn](#cfn-codegurureviewer-repositoryassociation-connectionarn): String
  [Name](#cfn-codegurureviewer-repositoryassociation-name): String
  [Owner](#cfn-codegurureviewer-repositoryassociation-owner): String
  [Tags](#cfn-codegurureviewer-repositoryassociation-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-codegurureviewer-repositoryassociation-type): String
```

## Properties<a name="aws-resource-codegurureviewer-repositoryassociation-properties"></a>

`ConnectionArn`  <a name="cfn-codegurureviewer-repositoryassociation-connectionarn"></a>
 The Amazon Resource Name \(ARN\) of an AWS CodeStar Connections connection\. Its format is `arn:aws:codestar-connections:region-id:aws-account_id:connection/connection-id`\. For more information, see [Connection](https://docs.aws.amazon.com/codestar-connections/latest/APIReference/API_Connection.html) in the *AWS CodeStar Connections API Reference*\.   
 `ConnectionArn` must be specified for Bitbucket and GitHub Enterprise Server repositories\. It has no effect if it is specified for an AWS CodeCommit repository\.   
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `256`  
*Pattern*: `arn:aws(-[\w]+)*:.+:.+:[0-9]{12}:.+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-codegurureviewer-repositoryassociation-name"></a>
The name of the repository\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^\S[\w.-]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Owner`  <a name="cfn-codegurureviewer-repositoryassociation-owner"></a>
 The owner of the repository\. For a GitHub Enterprise Server or Bitbucket repository, this is the username for the account that owns the repository\.   
 `Owner` must be specified for Bitbucket and GitHub Enterprise Server repositories\. It has no effect if it is specified for an AWS CodeCommit repository\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^\S(.*\S)?$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-codegurureviewer-repositoryassociation-tags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-codegurureviewer-repositoryassociation-type"></a>
 The type of repository that contains the source code to be reviewed\. The valid values are:   
+ `CodeCommit`
+ `Bitbucket`
+ `GitHubEnterpriseServer`
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-codegurureviewer-repositoryassociation-return-values"></a>

### Ref<a name="aws-resource-codegurureviewer-repositoryassociation-return-values-ref"></a>

 When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the Amazon Resource Name \(ARN\) of the AWS CodeGuru Reviewer [https://docs.aws.amazon.com/codeguru/latest/reviewer-api/API_RepositoryAssociation.html](https://docs.aws.amazon.com/codeguru/latest/reviewer-api/API_RepositoryAssociation.html), such as `arn:aws:codeguru-reviewer:region:123456789012:association/universally-unique-identifier`\. 

 For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\. 

### Fn::GetAtt<a name="aws-resource-codegurureviewer-repositoryassociation-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following is the available sample return values\. For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. 

#### <a name="aws-resource-codegurureviewer-repositoryassociation-return-values-fn--getatt-fn--getatt"></a>

`AssociationArn`  <a name="AssociationArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the [https://docs.aws.amazon.com/codeguru/latest/reviewer-api/API_RepositoryAssociation.html](https://docs.aws.amazon.com/codeguru/latest/reviewer-api/API_RepositoryAssociation.html) object\. You can retrieve this ARN by calling `ListRepositories`\.

## Examples<a name="aws-resource-codegurureviewer-repositoryassociation--examples"></a>



### Create an AWS CodeCommit repository association using an existing CodeCommit repository<a name="aws-resource-codegurureviewer-repositoryassociation--examples--Create_an_AWS_CodeCommit_repository_association_using_an_existing_CodeCommit_repository"></a>

The following example creates an Amazon CodeGuru Reviewer repository association using an existing AWS CodeCommit repository named `MyRepository`\.

#### YAML<a name="aws-resource-codegurureviewer-repositoryassociation--examples--Create_an_AWS_CodeCommit_repository_association_using_an_existing_CodeCommit_repository--yaml"></a>

```
Resources:
  MyRepositoryAssociation:
    Type: AWS::CodeGuruReviewer::RepositoryAssociation
    Properties:
      Name: MyRepository
      Type: CodeCommit
```

#### JSON<a name="aws-resource-codegurureviewer-repositoryassociation--examples--Create_an_AWS_CodeCommit_repository_association_using_an_existing_CodeCommit_repository--json"></a>

```
{
  "Resources": {
    "MyRepositoryAssociation": {
      "Type": "AWS::CodeGuruReviewer::RepositoryAssociation",
      "Properties": {
        "Name": "MyRepository",
        "Type": "CodeCommit"
      }
    }
  }
}
```

### Create an AWS CodeCommit repository association with a new CodeCommit repository<a name="aws-resource-codegurureviewer-repositoryassociation--examples--Create_an_AWS_CodeCommit_repository_association_with_a_new_CodeCommit_repository"></a>

The following example creates an AWS CodeCommit repository named `MyRepositoryName`\. Next, it creates an Amazon CodeGuru Reviewer repository association using the CodeCommit repository\. The `DependsOn` property in the `RepositoryAssociation` specifies the CodeCommit repository\. This is because the repository association can be created only after the CodeCommit repository is created\.

#### YAML<a name="aws-resource-codegurureviewer-repositoryassociation--examples--Create_an_AWS_CodeCommit_repository_association_with_a_new_CodeCommit_repository--yaml"></a>

```
Resources:
  MyRepository:
    Type: AWS::CodeCommit::Repository
    Properties:
      RepositoryName: MyRepositoryName
  MyRepositoryAssociation:
    Type: AWS::CodeGuruReviewer::RepositoryAssociation
    Properties:
      Name: MyRepositoryName
      Type: CodeCommit
    DependsOn: MyRepository
```

#### JSON<a name="aws-resource-codegurureviewer-repositoryassociation--examples--Create_an_AWS_CodeCommit_repository_association_with_a_new_CodeCommit_repository--json"></a>

```
{
  "Resources": {
    "MyRepository": {
      "Type": "AWS::CodeCommit::Repository",
      "Properties": {
        "RepositoryName": "MyRepositoryName"
      }
    },
    "MyRepositoryAssociation": {
      "Type": "AWS::CodeGuruReviewer::RepositoryAssociation",
      "Properties": {
        "Name": "MyRepositoryName",
        "Type": "CodeCommit"
      },
      "DependsOn": "MyRepository"
    }
  }
}
```

### Create a Bitbucket repository association<a name="aws-resource-codegurureviewer-repositoryassociation--examples--Create_a_Bitbucket_repository_association"></a>

The following example creates an Amazon CodeGuru Reviewer repository association using a Bitbucket repository\.

#### YAML<a name="aws-resource-codegurureviewer-repositoryassociation--examples--Create_a_Bitbucket_repository_association--yaml"></a>

```
Resources:
  MyRepositoryAssociation:
    Type: AWS::CodeGuruReviewer::RepositoryAssociation
    Properties:
      Name: MyBitbucketRepoName
      Type: Bitbucket
      ConnectionArn: arn:aws:codestar-connections:us-west-2:123456789012:connection/aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee
      Owner: MyOwnerName
```

#### JSON<a name="aws-resource-codegurureviewer-repositoryassociation--examples--Create_a_Bitbucket_repository_association--json"></a>

```
{
  "Resources": {
    "MyRepositoryAssociation": {
      "Type": "AWS::CodeGuruReviewer::RepositoryAssociation",
      "Properties": {
        "Name": "MyRepository",
        "Type": "CodeCommit"
      }
    }
  }
}
```

### Create a GitHub Enterprise Server repository association<a name="aws-resource-codegurureviewer-repositoryassociation--examples--Create_a_GitHub_Enterprise_Server_repository_association"></a>

The following example creates an Amazon CodeGuru Reviewer repository association using a GitHub Enterprise Server repository\.

#### YAML<a name="aws-resource-codegurureviewer-repositoryassociation--examples--Create_a_GitHub_Enterprise_Server_repository_association--yaml"></a>

```
Resources:
  MyRepositoryAssociation:
    Type: AWS::CodeGuruReviewer::RepositoryAssociation
    Properties:
      Name: MyGitHubEnterpriseRepoName
      Type: GitHubEnterpriseServer
      ConnectionArn: arn:aws:codestar-connections:us-west-2:123456789012:connection/aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee
      Owner: MyOwnerName
```

#### JSON<a name="aws-resource-codegurureviewer-repositoryassociation--examples--Create_a_GitHub_Enterprise_Server_repository_association--json"></a>

```
{
  "Resources": {
    "MyRepositoryAssociation": {
      "Type": "AWS::CodeGuruReviewer::RepositoryAssociation",
      "Properties": {
        "Name": "MyGitHubEnterpriseRepoName",
        "Type": "GitHubEnterpriseServer",
        "ConnectionArn": "arn:aws:codestar-connections:us-west-2:123456789012:connection/aaaaaaaa-bbbb-cccc-dddd-eeeeeeeeeeee",
        "Owner": "MyOwnerName"
      }
    }
  }
}
```