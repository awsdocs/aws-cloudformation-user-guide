# AWS::StepFunctions::Activity<a name="aws-resource-stepfunctions-activity"></a>

Use the `AWS::StepFunctions::Activity` resource to create an AWS Step Functions activity\.

For information about creating an activity and creating a state machine with an activity, see [Tutorial: An Activity State Machine](https://docs.aws.amazon.com/step-functions/latest/dg/activity-tutorial.html) in the *AWS Step Functions Developer Guide* and `[CreateActivity](https://docs.aws.amazon.com/step-functions/latest/apireference/API_CreateActivity.html)` in the *AWS Step Functions API Reference*\.

## Syntax<a name="aws-resource-stepfunctions-activity-syntax"></a>

### JSON<a name="aws-resource-stepfunctions-activity-syntax.json"></a>

```
{
   "Type": "AWS::StepFunctions::Activity",
   "Properties": {
      "[Name](#cfn-stepfunctions-activity-name)": String,
      "[Tags](#cfn-stepfunctions-activity-tags)" : [ Resource Tag, ... ] 
    }
}
```

### YAML<a name="aws-resource-stepfunctions-activity-syntax.yaml"></a>

```
Type: "AWS::StepFunctions::Activity"
Properties:
  [Name](#cfn-stepfunctions-activity-name): String
  [Tags](#cfn-stepfunctions-activity-tags):
    - Resource Tag
```

## Properties<a name="aws-resource-stepfunctions-activity-properties"></a>

`Name`  <a name="cfn-stepfunctions-activity-name"></a>
The name of the activity to create\. This name must be unique for your AWS account and region\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-stepfunctions-activity-tags"></a>
An array of key\-value pairs\. For more information, see [Using Cost Allocation Tags](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/cost-alloc-tags.html) in the *AWS Billing and Cost Management User Guide*, and [Controlling Access Using IAM Tags](https://docs.aws.amazon.com/IAM/latest/UserGuide/access_iam-tags.html)\.  
 *Required*: No  
 *Type*: List of [Resource Tag](aws-properties-resource-tags.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-stepfunctions-activity-return.yaml"></a>

### Ref<a name="aws-resource-stepfunctions-activity-return.yaml.ref"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the ARN of the created activity\. For example:

```
{ "Ref": "MyActivity" }
```

Returns a value similar to the following:

```
arn:aws:states:us-east-1:111122223333:activity:myActivity
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-stepfunctions-activity-return.getatt"></a>

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

## Example<a name="aws-resource-stepfunctions-activity-example"></a>

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
            "Name" : "myActivity",
            "Tags": [
                    {
                        "Key": "keyname1",
                        "Value": "value1"
                    },
                    {
                        "Key": "keyname2",
                        "Value": "value2"
                    }
                ]
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
      Tags:
        -
          Key: "keyname1"
          Value: "value1"
        -
          Key: "keyname2"
          Value: "value2"
```