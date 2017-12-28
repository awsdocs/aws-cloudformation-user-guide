# AWS CodeCommit Repository Trigger<a name="aws-properties-codecommit-repository-triggers"></a>

`Trigger` is a property of the [AWS::CodeCommit::Repository](aws-resource-codecommit-repository.md) resource that defines the actions to take in response to events that occur in the AWS CodeCommit repository\.

## Syntax<a name="aws-properties-codecommit-repository-triggers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codecommit-repository-triggers-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codecommit-repository-triggers-branches)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codecommit-repository-triggers-customdata)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codecommit-repository-triggers-destinationarn)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codecommit-repository-triggers-events)" : [ String, ... ],
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-codecommit-repository-triggers-name)" : String
}
```

### YAML<a name="aws-properties-codecommit-repository-triggers-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codecommit-repository-triggers-branches):
- String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codecommit-repository-triggers-customdata): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codecommit-repository-triggers-destinationarn): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codecommit-repository-triggers-events):
- String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-codecommit-repository-triggers-name): String
```

## Properties<a name="w3ab2c21c14d307b7"></a>

`Branches`  
The names of the branches in the AWS CodeCommit repository that contain events that you want to include in the trigger\. If you don't specify at least one branch, the trigger applies to all branches\.  
*Required: *No  
*Type*: List of String values

`CustomData`  
When an event is triggered, additional information that AWS CodeCommit includes when it sends information to the target\.  
*Required: *No  
*Type*: String

`DestinationArn`  
The Amazon Resource Name \(ARN\) of the resource that is the target for this trigger\. For valid targets, see [Manage Triggers for an AWS CodeCommit Repository](http://docs.aws.amazon.com/codecommit/latest/userguide/how-to-notify.html) in the *AWS CodeCommit User Guide*\.  
*Required: *No  
*Type*: String

`Events`  
The repository events for which AWS CodeCommit sends information to the target, which you specified in the `DestinationArn` property\. If you don't specify events, the trigger runs for all repository events\. For valid values, see the [RepositoryTrigger](http://docs.aws.amazon.com/codecommit/latest/APIReference/API_RepositoryTrigger.html) data type in the *AWS CodeCommit API Reference*\.  
*Required: *No  
*Type*: List of String values

`Name`  
A name for the trigger\.  
*Required: *Yes  
*Type*: String