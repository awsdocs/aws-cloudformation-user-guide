# AWS::Glue::Trigger Action<a name="aws-properties-glue-trigger-action"></a>

Defines an action to be initiated by a trigger\.

## Syntax<a name="aws-properties-glue-trigger-action-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-trigger-action-syntax.json"></a>

```
{
  "[Arguments](#cfn-glue-trigger-action-arguments)" : Json,
  "[JobName](#cfn-glue-trigger-action-jobname)" : String
}
```

### YAML<a name="aws-properties-glue-trigger-action-syntax.yaml"></a>

```
﻿  [Arguments](#cfn-glue-trigger-action-arguments) : Json
﻿  [JobName](#cfn-glue-trigger-action-jobname) : String
```

## Properties<a name="aws-properties-glue-trigger-action-properties"></a>

`Arguments`  <a name="cfn-glue-trigger-action-arguments"></a>
The job arguments used when this trigger fires\. For this job run, they replace the default arguments set in the job definition itself\.  
You can specify arguments here that your own job\-execution script consumes, in addition to arguments that AWS Glue itself consumes\.  
For information about how to specify and consume your own job arguments, see [Calling AWS Glue APIs in Python](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-programming-python-calling.html) in the *AWS Glue Developer Guide*\.  
For information about the key\-value pairs that AWS Glue consumes to set up your job, see the [Special Parameters Used by AWS Glue](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-programming-etl-glue-arguments.html) topic in the developer guide\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JobName`  <a name="cfn-glue-trigger-action-jobname"></a>
The name of a job to be executed\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-properties-glue-trigger-action--seealso"></a>
+  [Action Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-jobs-trigger.html#aws-glue-api-jobs-trigger-Action) in the *AWS Glue Developer Guide* 