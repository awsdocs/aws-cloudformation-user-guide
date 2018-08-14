# AWS::StepFunctions::Activity<a name="aws-resource-stepfunctions-activity"></a>

Use the `AWS::StepFunctions::Activity` resource to create an AWS Step Functions activity\.

For information about creating an activity and creating a state machine with an activity, see [Tutorial: An Activity State Machine](http://docs.aws.amazon.com/step-functions/latest/dg/activity-tutorial.html) in the *AWS Step Functions Developer Guide* and `[CreateActivity](http://docs.aws.amazon.com/step-functions/latest/apireference/API_CreateActivity.html)` in the *AWS Step Functions API Reference*\.

## Syntax<a name="w3ab2c21c10e1176b7"></a>

### JSON<a name="aws-resource-stepfunctions-activity-syntax.json"></a>

```
{
   "Type": "AWS::StepFunctions::Activity",
   "Properties": {
      "[Name](#cfn-stepfunctions-activity-name)": String
    }
}
```

### YAML<a name="aws-resource-stepfunctions-activity-syntax.yaml"></a>

```
Type: "AWS::StepFunctions::Activity"
Properties:
  [Name](#cfn-stepfunctions-activity-name): String
```

## Properties<a name="w3ab2c21c10e1176b9"></a>

`Name`  <a name="cfn-stepfunctions-activity-name"></a>
The name of the activity to create\. This name must be unique for your AWS account and region\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10e1176c11"></a>

### Ref<a name="w3ab2c21c10e1176c11b2"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the ARN of the created activity\. For example:

```
{ "Ref": "MyActivity" }
```

Returns a value similar to the following:

```
arn:aws:states:us-east-1:111122223333:activity:myActivity
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10e1176c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Name`  
Returns the name of the activity\. For example:  

```
{ "Fn::GetAtt": ["MyActivity", "Name"] }
```
Returns a value similar to the following:  

```
myActivity
```

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Example<a name="w3ab2c21c10e1176c13"></a>

The following example creates a Step Functions activity\.

### JSON<a name="aws-resource-stepfunctions-activity-example.json"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Description" : "An example template for a Step Functions activity.",
   "Resources" : {
      "MyActivity" : {
         "Type" : "AWS::StepFunctions::Activity",
         "Properties" : {
            "Name" : "myActivity"
        }
      }
   }
}
```

### YAML<a name="aws-resource-stepfunctions-activity-example.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Description: "A sample template for a Step Functions activity"
Resources: 
  MyActivity:
    Type: "AWS::StepFunctions::Activity"
    Properties: 
      Name: myActivity
```