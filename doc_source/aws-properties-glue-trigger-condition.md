# AWS::Glue::Trigger Condition<a name="aws-properties-glue-trigger-condition"></a>

Defines a condition under which a trigger fires\.

## Syntax<a name="aws-properties-glue-trigger-condition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-trigger-condition-syntax.json"></a>

```
{
  "[JobName](#cfn-glue-trigger-condition-jobname)" : String,
  "[LogicalOperator](#cfn-glue-trigger-condition-logicaloperator)" : String,
  "[State](#cfn-glue-trigger-condition-state)" : String
}
```

### YAML<a name="aws-properties-glue-trigger-condition-syntax.yaml"></a>

```
﻿  [JobName](#cfn-glue-trigger-condition-jobname) : String
﻿  [LogicalOperator](#cfn-glue-trigger-condition-logicaloperator) : String
﻿  [State](#cfn-glue-trigger-condition-state) : String
```

## Properties<a name="aws-properties-glue-trigger-condition-properties"></a>

`JobName`  <a name="cfn-glue-trigger-condition-jobname"></a>
The name of the job whose `JobRuns` this condition applies to, and on which this trigger waits\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogicalOperator`  <a name="cfn-glue-trigger-condition-logicaloperator"></a>
A logical operator\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-glue-trigger-condition-state"></a>
The condition state\. Currently, the values supported are `SUCCEEDED`, `STOPPED`, `TIMEOUT`, and `FAILED`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-glue-trigger-condition--seealso"></a>
+  [Condition Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-trigger.html#aws-glue-api-jobs-trigger-Condition) in the *AWS Glue Developer Guide* 