# AWS::DLM::LifecyclePolicy<a name="aws-resource-dlm-lifecyclepolicy"></a>

Specifies a lifecycle policy, which is used to automate operations on Amazon EBS resources\.

The properties are required when you add a lifecycle policy and optional when you update a lifecycle policy\.

## Syntax<a name="aws-resource-dlm-lifecyclepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dlm-lifecyclepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::DLM::LifecyclePolicy",
  "Properties" : {
      "[Description](#cfn-dlm-lifecyclepolicy-description)" : String,
      "[ExecutionRoleArn](#cfn-dlm-lifecyclepolicy-executionrolearn)" : String,
      "[PolicyDetails](#cfn-dlm-lifecyclepolicy-policydetails)" : PolicyDetails,
      "[State](#cfn-dlm-lifecyclepolicy-state)" : String,
      "[Tags](#cfn-dlm-lifecyclepolicy-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-dlm-lifecyclepolicy-syntax.yaml"></a>

```
Type: AWS::DLM::LifecyclePolicy
Properties: 
  [Description](#cfn-dlm-lifecyclepolicy-description): String
  [ExecutionRoleArn](#cfn-dlm-lifecyclepolicy-executionrolearn): String
  [PolicyDetails](#cfn-dlm-lifecyclepolicy-policydetails): 
    PolicyDetails
  [State](#cfn-dlm-lifecyclepolicy-state): String
  [Tags](#cfn-dlm-lifecyclepolicy-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-dlm-lifecyclepolicy-properties"></a>

`Description`  <a name="cfn-dlm-lifecyclepolicy-description"></a>
A description of the lifecycle policy\. The characters ^\[0\-9A\-Za\-z \_\-\]\+$ are supported\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `500`  
*Pattern*: `[0-9A-Za-z _-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExecutionRoleArn`  <a name="cfn-dlm-lifecyclepolicy-executionrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role used to run the operations specified by the lifecycle policy\.  
*Required*: Conditional  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Pattern*: `arn:aws(-[a-z]{1,3}){0,2}:iam::\d+:role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PolicyDetails`  <a name="cfn-dlm-lifecyclepolicy-policydetails"></a>
The configuration details of the lifecycle policy\.  
*Required*: Conditional  
*Type*: [PolicyDetails](aws-properties-dlm-lifecyclepolicy-policydetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-dlm-lifecyclepolicy-state"></a>
The activation state of the lifecycle policy\.  
*Required*: Conditional  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED | ERROR`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-dlm-lifecyclepolicy-tags"></a>
The tags to apply to the lifecycle policy during creation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-dlm-lifecyclepolicy-return-values"></a>

### Ref<a name="aws-resource-dlm-lifecyclepolicy-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the lifecycle policy\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-dlm-lifecyclepolicy-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-dlm-lifecyclepolicy-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the lifecycle policy\.

## Examples<a name="aws-resource-dlm-lifecyclepolicy--examples"></a>

### Creating a Lifecycle Policy<a name="aws-resource-dlm-lifecyclepolicy--examples--Creating_a_Lifecycle_Policy"></a>

The following example demonstrates how to create a basic lifecycle policy\.

#### YAML<a name="aws-resource-dlm-lifecyclepolicy--examples--Creating_a_Lifecycle_Policy--yaml"></a>

```
Description: "Basic LifecyclePolicy"
Resources:
  BasicLifecyclePolicy:
    Type: "AWS::DLM::LifecyclePolicy"
    Properties:
      Description: "Lifecycle Policy using CloudFormation"
      State: "ENABLED"
      ExecutionRoleArn: "arn:aws:iam::123456789012:role/AWSDataLifecycleManagerDefaultRole"
      PolicyDetails:
        ResourceTypes:
          - "VOLUME"
        TargetTags:
          -
            Key: "costcenter"
            Value: "115"
          
        Schedules:
          -
            Name: "Daily Snapshots"
            TagsToAdd:
              -
                Key: "type"
                Value: "DailySnapshot"
              
            CreateRule:
              Interval: 12
              IntervalUnit: "HOURS"
              Times:
                - "13:00"
            RetainRule:
              Count: 1
            CopyTags: true
```

#### JSON<a name="aws-resource-dlm-lifecyclepolicy--examples--Creating_a_Lifecycle_Policy--json"></a>

```
{
    "Description": "Basic LifecyclePolicy",
    "Resources": {
        "BasicLifecyclePolicy": {
            "Type": "AWS::DLM::LifecyclePolicy",
            "Properties": {
                "Description": "Lifecycle Policy using CloudFormation",
                "State": "ENABLED",
                "ExecutionRoleArn": "arn:aws:iam::123456789012:role/AWSDataLifecycleManagerDefaultRole",
                "PolicyDetails": {
                    "ResourceTypes": [
                        "VOLUME"
                    ],
                    "TargetTags": [
                        {
                            "Key": "costcenter",
                            "Value": "115"
                        }
                    ],
                    "Schedules": [
                        {
                            "Name": "Daily Snapshots",
                            "TagsToAdd": [
                                {
                                    "Key": "type",
                                    "Value": "DailySnapshot"
                                }
                            ],
                            "CreateRule": {
                                "Interval": 12,
                                "IntervalUnit": "HOURS",
                                "Times": [
                                    "13:00"
                                ]
                            },
                            "RetainRule": {
                                "Count": 1
                            },
                            "CopyTags": true
                        }
                    ]
                }
            }
        }
    }
```

## See also<a name="aws-resource-dlm-lifecyclepolicy--seealso"></a>
+  [CreateLifecyclePolicy](https://docs.aws.amazon.com/dlm/latest/APIReference/API_CreateLifecyclePolicy.html) in the *Amazon Data Lifecycle Manager API Reference* 
+  [Automating the Amazon EBS Snapshot Lifecycle](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-lifecycle.html) in the *Amazon Elastic Compute Cloud User Guide* 

