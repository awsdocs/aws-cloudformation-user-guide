# AWS CodeCommit Repository Trigger<a name="aws-properties-codecommit-repository-triggers"></a>

`Trigger` is a property of the [AWS::CodeCommit::Repository](aws-resource-codecommit-repository.md) resource that defines the actions to take in response to events that occur in the AWS CodeCommit repository\.

## Syntax<a name="aws-properties-codecommit-repository-triggers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-codecommit-repository-triggers-syntax.json"></a>

```
{
  "[Branches](#cfn-codecommit-repository-triggers-branches)" : [ String, ... ],
  "[CustomData](#cfn-codecommit-repository-triggers-customdata)" : String,
  "[DestinationArn](#cfn-codecommit-repository-triggers-destinationarn)" : String,
  "[Events](#cfn-codecommit-repository-triggers-events)" : [ String, ... ],
  "[Name](#cfn-codecommit-repository-triggers-name)" : String
}
```

### YAML<a name="aws-properties-codecommit-repository-triggers-syntax.yaml"></a>

```
[Branches](#cfn-codecommit-repository-triggers-branches):
- String
[CustomData](#cfn-codecommit-repository-triggers-customdata): String
[DestinationArn](#cfn-codecommit-repository-triggers-destinationarn): String
[Events](#cfn-codecommit-repository-triggers-events):
- String
[Name](#cfn-codecommit-repository-triggers-name): String
```

## Properties<a name="w3ab2c21c14d381b7"></a>

`Branches`  <a name="cfn-codecommit-repository-triggers-branches"></a>
The names of the branches in the AWS CodeCommit repository that contain events that you want to include in the trigger\. If you don't specify at least one branch, the trigger applies to all branches\.  
*Required*: No  
*Type*: List of String values

`CustomData`  <a name="cfn-codecommit-repository-triggers-customdata"></a>
When an event is triggered, additional information that AWS CodeCommit includes when it sends information to the target\.  
*Required*: No  
*Type*: String

`DestinationArn`  <a name="cfn-codecommit-repository-triggers-destinationarn"></a>
The Amazon Resource Name \(ARN\) of the resource that is the target for this trigger\. For valid targets, see [Manage Triggers for an AWS CodeCommit Repository](http://docs.aws.amazon.com/codecommit/latest/userguide/how-to-notify.html) in the *AWS CodeCommit User Guide*\.  
*Required*: No  
*Type*: String

`Events`  <a name="cfn-codecommit-repository-triggers-events"></a>
The repository events for which AWS CodeCommit sends information to the target, which you specified in the `DestinationArn` property\. If you don't specify events, the trigger runs for all repository events\. For valid values, see the [RepositoryTrigger](http://docs.aws.amazon.com/codecommit/latest/APIReference/API_RepositoryTrigger.html) data type in the *AWS CodeCommit API Reference*\.  
*Required*: No  
*Type*: List of String values

`Name`  <a name="cfn-codecommit-repository-triggers-name"></a>
A name for the trigger\.  
*Required*: Yes  
*Type*: String