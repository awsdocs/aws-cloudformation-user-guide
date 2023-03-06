# AWS::CloudFormation::StackSet ManagedExecution<a name="aws-properties-cloudformation-stackset-managedexecution"></a>

Describes whether StackSets performs non\-conflicting operations concurrently and queues conflicting operations\.

## Syntax<a name="aws-properties-cloudformation-stackset-managedexecution-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudformation-stackset-managedexecution-syntax.json"></a>

```
{
  "[Active](#cfn-cloudformation-stackset-managedexecution-active)" : Boolean
}
```

### YAML<a name="aws-properties-cloudformation-stackset-managedexecution-syntax.yaml"></a>

```
  [Active](#cfn-cloudformation-stackset-managedexecution-active): Boolean
```

## Properties<a name="aws-properties-cloudformation-stackset-managedexecution-properties"></a>

`Active`  <a name="cfn-cloudformation-stackset-managedexecution-active"></a>
When `true`, StackSets performs non\-conflicting operations concurrently and queues conflicting operations\. After conflicting operations finish, StackSets starts queued operations in request order\.  
If there are already running or queued operations, StackSets queues all incoming operations even if they are non\-conflicting\.  
You can't modify your stack set's execution configuration while there are running or queued operations for that stack set\.
When `false` \(default\), StackSets performs one operation at a time in request order\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)