# AWS::ECS::CapacityProvider<a name="aws-resource-ecs-capacityprovider"></a>

The `AWS::ECS::CapacityProvider` resource creates an Amazon Elastic Container Service \(Amazon ECS\) capacity provider\. Capacity providers are associated with an Amazon ECS cluster and are used in capacity provider strategies to facilitate cluster auto scaling\.

Only capacity providers using an Auto Scaling group can be created\. Amazon ECS tasks on AWS Fargate use the `FARGATE` and `FARGATE_SPOT` capacity providers which are already created and available to all accounts in Regions supported by AWS Fargate\.

## Syntax<a name="aws-resource-ecs-capacityprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecs-capacityprovider-syntax.json"></a>

```
{
  "Type" : "AWS::ECS::CapacityProvider",
  "Properties" : {
      "[AutoScalingGroupProvider](#cfn-ecs-capacityprovider-autoscalinggroupprovider)" : AutoScalingGroupProvider,
      "[Name](#cfn-ecs-capacityprovider-name)" : String,
      "[Tags](#cfn-ecs-capacityprovider-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ecs-capacityprovider-syntax.yaml"></a>

```
Type: AWS::ECS::CapacityProvider
Properties: 
  [AutoScalingGroupProvider](#cfn-ecs-capacityprovider-autoscalinggroupprovider): 
    AutoScalingGroupProvider
  [Name](#cfn-ecs-capacityprovider-name): String
  [Tags](#cfn-ecs-capacityprovider-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ecs-capacityprovider-properties"></a>

`AutoScalingGroupProvider`  <a name="cfn-ecs-capacityprovider-autoscalinggroupprovider"></a>
The Auto Scaling group settings for the capacity provider\.  
*Required*: Yes  
*Type*: [AutoScalingGroupProvider](aws-properties-ecs-capacityprovider-autoscalinggroupprovider.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-ecs-capacityprovider-name"></a>
The name of the capacity provider\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ecs-capacityprovider-tags"></a>
The metadata that you apply to the capacity provider to help you categorize and organize it\. Each tag consists of a key and an optional value, both of which you define\.  
The following basic restrictions apply to tags:  
+ Maximum number of tags per resource \- 50
+ For each resource, each tag key must be unique, and each tag key can have only one value\.
+ Maximum key length \- 128 Unicode characters in UTF\-8
+ Maximum value length \- 256 Unicode characters in UTF\-8
+ If your tagging schema is used across multiple services and resources, remember that other services may have restrictions on allowed characters\. Generally allowed characters are: letters, numbers, and spaces representable in UTF\-8, and the following characters: \+ \- = \. \_ : / @\.
+ Tag keys and values are case\-sensitive\.
+ Do not use `aws:`, `AWS:`, or any upper or lowercase combination of such as a prefix for either keys or values as it is reserved for AWS use\. You cannot edit or delete tag keys or values with this prefix\. Tags with this prefix do not count against your tags per resource limit\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ecs-capacityprovider-return-values"></a>

### Ref<a name="aws-resource-ecs-capacityprovider-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

In the following example, the `Ref` function returns the name of the capacity provider, such as `MyStack-MyCapacityProvider-JrwYBzxovGfr`\.

 `{ "Ref": "MyCapacityProvider" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ecs-capacityprovider--examples"></a>



### Creating an Amazon ECS capacity provider<a name="aws-resource-ecs-capacityprovider--examples--Creating_an_Amazon_ECS_capacity_provider"></a>

The following example creates a capacity provider that uses the Auto Scaling group `MyAutoScalingGroup`, has managed scaling and managed termination protection enabled\. This configuration is used for Amazon ECS cluster auto scaling\.

#### JSON<a name="aws-resource-ecs-capacityprovider--examples--Creating_an_Amazon_ECS_capacity_provider--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "ECSCapacityProvider": {
            "Type": "AWS::ECS::CapacityProvider",
            "Properties": {
                "AutoScalingGroupProvider": {
                    "AutoScalingGroupArn": "arn:aws:autoscaling:us-west-2:123456789012:autoScalingGroup:a1b2c3d4-5678-90ab-cdef-EXAMPLE11111:autoScalingGroupName/MyAutoScalingGroup",
                    "ManagedScaling": {
                        "MaximumScalingStepSize": 10,
                        "MinimumScalingStepSize": 1,
                        "Status": "ENABLED",
                        "TargetCapacity": 100
                    },
                    "ManagedTerminationProtection": "ENABLED"
                },
                "Tags": [
                    {
                        "Key": "environment",
                        "Value": "production"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ecs-capacityprovider--examples--Creating_an_Amazon_ECS_capacity_provider--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  ECSCapacityProvider:
    Type: AWS::ECS::CapacityProvider
    Properties:
        AutoScalingGroupProvider:
            AutoScalingGroupArn: arn:aws:autoscaling:us-west-2:123456789012:autoScalingGroup:a1b2c3d4-5678-90ab-cdef-EXAMPLE11111:autoScalingGroupName/MyAutoScalingGroup
            ManagedScaling:
                MaximumScalingStepSize: 10
                MinimumScalingStepSize: 1
                Status: ENABLED
                TargetCapacity: 100
            ManagedTerminationProtection: ENABLED
        Tags:
            - Key: environment
              Value: production
```