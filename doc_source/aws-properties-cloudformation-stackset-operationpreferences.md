# AWS::CloudFormation::StackSet OperationPreferences<a name="aws-properties-cloudformation-stackset-operationpreferences"></a>

The user\-specified preferences for how AWS CloudFormation performs a stack set operation\. For more information on maximum concurrent accounts and failure tolerance, see [Stack set operation options](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-concepts.html#stackset-ops-options)\.

## Syntax<a name="aws-properties-cloudformation-stackset-operationpreferences-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cloudformation-stackset-operationpreferences-syntax.json"></a>

```
{
  "[FailureToleranceCount](#cfn-cloudformation-stackset-operationpreferences-failuretolerancecount)" : Integer,
  "[FailureTolerancePercentage](#cfn-cloudformation-stackset-operationpreferences-failuretolerancepercentage)" : Integer,
  "[MaxConcurrentCount](#cfn-cloudformation-stackset-operationpreferences-maxconcurrentcount)" : Integer,
  "[MaxConcurrentPercentage](#cfn-cloudformation-stackset-operationpreferences-maxconcurrentpercentage)" : Integer,
  "[RegionOrder](#cfn-cloudformation-stackset-operationpreferences-regionorder)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-cloudformation-stackset-operationpreferences-syntax.yaml"></a>

```
  [FailureToleranceCount](#cfn-cloudformation-stackset-operationpreferences-failuretolerancecount): Integer
  [FailureTolerancePercentage](#cfn-cloudformation-stackset-operationpreferences-failuretolerancepercentage): Integer
  [MaxConcurrentCount](#cfn-cloudformation-stackset-operationpreferences-maxconcurrentcount): Integer
  [MaxConcurrentPercentage](#cfn-cloudformation-stackset-operationpreferences-maxconcurrentpercentage): Integer
  [RegionOrder](#cfn-cloudformation-stackset-operationpreferences-regionorder): 
    - String
```

## Properties<a name="aws-properties-cloudformation-stackset-operationpreferences-properties"></a>

`FailureToleranceCount`  <a name="cfn-cloudformation-stackset-operationpreferences-failuretolerancecount"></a>
The number of accounts, per Region, for which this operation can fail before AWS CloudFormation stops the operation in that Region\. If the operation is stopped in a Region, AWS CloudFormation doesn't attempt the operation in any subsequent Regions\.  
Conditional: You must specify either `FailureToleranceCount` or `FailureTolerancePercentage` \(but not both\)\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailureTolerancePercentage`  <a name="cfn-cloudformation-stackset-operationpreferences-failuretolerancepercentage"></a>
The percentage of accounts, per Region, for which this stack operation can fail before AWS CloudFormation stops the operation in that Region\. If the operation is stopped in a Region, AWS CloudFormation doesn't attempt the operation in any subsequent Regions\.  
When calculating the number of accounts based on the specified percentage, AWS CloudFormation rounds *down* to the next whole number\.  
Conditional: You must specify either `FailureToleranceCount` or `FailureTolerancePercentage`, but not both\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxConcurrentCount`  <a name="cfn-cloudformation-stackset-operationpreferences-maxconcurrentcount"></a>
The maximum number of accounts in which to perform this operation at one time\. This is dependent on the value of `FailureToleranceCount`\. `MaxConcurrentCount` is at most one more than the `FailureToleranceCount`\.  
Note that this setting lets you specify the *maximum* for operations\. For large deployments, under certain circumstances the actual number of accounts acted upon concurrently may be lower due to service throttling\.  
Conditional: You must specify either `MaxConcurrentCount` or `MaxConcurrentPercentage`, but not both\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxConcurrentPercentage`  <a name="cfn-cloudformation-stackset-operationpreferences-maxconcurrentpercentage"></a>
The maximum percentage of accounts in which to perform this operation at one time\.  
When calculating the number of accounts based on the specified percentage, AWS CloudFormation rounds down to the next whole number\. This is true except in cases where rounding down would result is zero\. In this case, CloudFormation sets the number as one instead\.  
Note that this setting lets you specify the *maximum* for operations\. For large deployments, under certain circumstances the actual number of accounts acted upon concurrently may be lower due to service throttling\.  
Conditional: You must specify either `MaxConcurrentCount` or `MaxConcurrentPercentage`, but not both\.  
*Required*: Conditional  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegionOrder`  <a name="cfn-cloudformation-stackset-operationpreferences-regionorder"></a>
The order of the Regions where you want to perform the stack operation\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)