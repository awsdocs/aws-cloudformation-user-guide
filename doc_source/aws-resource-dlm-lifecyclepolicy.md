# AWS::DLM::LifecyclePolicy<a name="aws-resource-dlm-lifecyclepolicy"></a>

The `AWS::DLM::LifecyclePolicy` resource creates a lifecycle policy for Amazon Data Lifecycle Manager\. For more information, see [Automating the Amazon EBS Snapshot Lifecycle](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-lifecycle.html) in the Amazon EC2 User Guide for Linux Instances and [CreateLifecyclePolicy](https://docs.aws.amazon.com/dlm/latest/APIReference/API_CreateLifecyclePolicy.html) in the [Amazon Data Lifecycle Manager API Reference](https://docs.aws.amazon.com/dlm/latest/APIReference/)\. 

## Syntax<a name="aws-resource-dlm-lifecyclepolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dlm-lifecyclepolicy-syntax.json"></a>

```
{
  "Type" : "AWS::DLM::LifecyclePolicy",
  "Properties" : {
    "[Description](#cfn-dlm-lifecyclepolicy-description)" : String,
    "[ExecutionRoleArn](#cfn-dlm-lifecyclepolicy-executionrolearn)" : String,
    "[PolicyDetails](#cfn-dlm-lifecyclepolicy-policydetails)" : [*PolicyDetails*](aws-properties-dlm-lifecyclepolicy-policydetails.md),
    "[State](#cfn-dlm-lifecyclepolicy-state)" : String
  }
}
```

### YAML<a name="aws-resource-dlm-lifecyclepolicy-syntax.yaml"></a>

```
Type: "AWS::DLM::LifecyclePolicy"
Properties:
  [Description](#cfn-dlm-lifecyclepolicy-description): String
  [ExecutionRoleArn](#cfn-dlm-lifecyclepolicy-executionrolearn): String
  [PolicyDetails](#cfn-dlm-lifecyclepolicy-policydetails): 
    [*PolicyDetails*](aws-properties-dlm-lifecyclepolicy-policydetails.md)
  [State](#cfn-dlm-lifecyclepolicy-state): String
```

## Properties<a name="aws-resource-dlm-lifecyclepolicy-properties"></a>

`Description`  <a name="cfn-dlm-lifecyclepolicy-description"></a>
The description of the lifecycle policy\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ExecutionRoleArn`  <a name="cfn-dlm-lifecyclepolicy-executionrolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role used to run the operations specified by the lifecycle policy\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`PolicyDetails`  <a name="cfn-dlm-lifecyclepolicy-policydetails"></a>
The configuration of the lifecycle policy\.  
 *Required*: No  
 *Type*: [PolicyDetails](aws-properties-dlm-lifecyclepolicy-policydetails.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`State`  <a name="cfn-dlm-lifecyclepolicy-state"></a>
The activation state of the lifecycle policy\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-dlm-lifecyclepolicy-returnvalues"></a>

### Ref<a name="aws-resource-dlm-lifecyclepolicy-ref"></a>

When you pass the logical ID of an `AWS::DLM::LifecyclePolicy` resource to the intrinsic `Ref` function, the function returns the policy ID, such as `policy-0123456789abcdef0`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-dlm-lifecyclepolicy-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the policy, such as `arn:aws:dlm:us-west-2:012345678912:policy/policy-0123456789abcdef`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## Examples<a name="aws-resource-dlm-lifecyclepolicy-examples"></a>

### Creating a Lifecycle Policy<a name="aws-resource-dlm-lifecyclepolicy-example1"></a>

The following example illustrates the creation of a basic lifecycle policy\.

#### JSON<a name="aws-resource-dlm-lifecyclepolicy-example1.json"></a>

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

#### YAML<a name="aws-resource-dlm-lifecyclepolicy-example1.yaml"></a>

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

## See Also<a name="aws-resource-dlm-lifecyclepolicy-seealso"></a>
+ [Automating the Amazon EBS Snapshot Lifecycle](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/snapshot-lifecycle.html) in the Amazon EC2 User Guide for Linux Instances
+ [CreateLifecyclePolicy](https://docs.aws.amazon.com/dlm/latest/APIReference/API_CreateLifecyclePolicy.html) in the Amazon Data Lifecycle Manager API Reference