# AWS::AppRunner::AutoScalingConfiguration<a name="aws-resource-apprunner-autoscalingconfiguration"></a>

The `AWS::AppRunner::AutoScalingConfiguration` resource is an AWS App Runner resource type that specifies an App Runner automatic scaling configuration\.

App Runner requires this resource to set non\-default auto scaling settings for instances used to process the web requests\. You can share an auto scaling configuration across multiple services\.

Create multiple revisions of a configuration by calling this action multiple times using the same `AutoScalingConfigurationName`\. The call returns incremental `AutoScalingConfigurationRevision` values\. When you create a service and configure an auto scaling configuration resource, the service uses the latest active revision of the auto scaling configuration by default\. You can optionally configure the service to use a specific revision\.

Configure a higher `MinSize` to increase the spread of your App Runner service over more Availability Zones in the AWS Region\. The tradeoff is a higher minimal cost\.

Configure a lower `MaxSize` to control your cost\. The tradeoff is lower responsiveness during peak demand\.

## Syntax<a name="aws-resource-apprunner-autoscalingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apprunner-autoscalingconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::AppRunner::AutoScalingConfiguration",
  "Properties" : {
      "[AutoScalingConfigurationName](#cfn-apprunner-autoscalingconfiguration-autoscalingconfigurationname)" : String,
      "[MaxConcurrency](#cfn-apprunner-autoscalingconfiguration-maxconcurrency)" : Integer,
      "[MaxSize](#cfn-apprunner-autoscalingconfiguration-maxsize)" : Integer,
      "[MinSize](#cfn-apprunner-autoscalingconfiguration-minsize)" : Integer,
      "[Tags](#cfn-apprunner-autoscalingconfiguration-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-apprunner-autoscalingconfiguration-syntax.yaml"></a>

```
Type: AWS::AppRunner::AutoScalingConfiguration
Properties: 
  [AutoScalingConfigurationName](#cfn-apprunner-autoscalingconfiguration-autoscalingconfigurationname): String
  [MaxConcurrency](#cfn-apprunner-autoscalingconfiguration-maxconcurrency): Integer
  [MaxSize](#cfn-apprunner-autoscalingconfiguration-maxsize): Integer
  [MinSize](#cfn-apprunner-autoscalingconfiguration-minsize): Integer
  [Tags](#cfn-apprunner-autoscalingconfiguration-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-apprunner-autoscalingconfiguration-properties"></a>

`AutoScalingConfigurationName`  <a name="cfn-apprunner-autoscalingconfiguration-autoscalingconfigurationname"></a>
The customer\-provided auto scaling configuration name\. It can be used in multiple revisions of a configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `4`  
*Maximum*: `32`  
*Pattern*: `[A-Za-z0-9][A-Za-z0-9\-_]{3,31}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxConcurrency`  <a name="cfn-apprunner-autoscalingconfiguration-maxconcurrency"></a>
The maximum number of concurrent requests that an instance processes\. If the number of concurrent requests exceeds this limit, App Runner scales the service up\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MaxSize`  <a name="cfn-apprunner-autoscalingconfiguration-maxsize"></a>
The maximum number of instances that a service scales up to\. At most `MaxSize` instances actively serve traffic for your service\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MinSize`  <a name="cfn-apprunner-autoscalingconfiguration-minsize"></a>
The minimum number of instances that App Runner provisions for a service\. The service always has at least `MinSize` provisioned instances\. Some of them actively serve traffic\. The rest of them \(provisioned and inactive instances\) are a cost\-effective compute capacity reserve and are ready to be quickly activated\. You pay for memory usage of all the provisioned instances\. You pay for CPU usage of only the active subset\.  
App Runner temporarily doubles the number of provisioned instances during deployments, to maintain the same capacity for both old and new code\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-apprunner-autoscalingconfiguration-tags"></a>
A list of metadata items that you can associate with your auto scaling configuration resource\. A tag is a key\-value pair\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-apprunner-autoscalingconfiguration-return-values"></a>

### Ref<a name="aws-resource-apprunner-autoscalingconfiguration-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref`intrinsic function, `Ref`returns the resource name\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-apprunner-autoscalingconfiguration-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-apprunner-autoscalingconfiguration-return-values-fn--getatt-fn--getatt"></a>

`AutoScalingConfigurationArn`  <a name="AutoScalingConfigurationArn-fn::getatt"></a>
 The Amazon Resource Name \(ARN\) of this auto scaling configuration\. 

`AutoScalingConfigurationRevision`  <a name="AutoScalingConfigurationRevision-fn::getatt"></a>
 The revision of this auto scaling configuration\. It's unique among all the active configurations that share the same `AutoScalingConfigurationName`\. 

`Latest`  <a name="Latest-fn::getatt"></a>
 It's set to true for the configuration with the highest `Revision` among all configurations that share the same `AutoScalingConfigurationName`\. It's set to false otherwise\. App Runner temporarily doubles the number of provisioned instances during deployments, to maintain the same capacity for both old and new code\. 

`Status`  <a name="Status-fn::getatt"></a>
 The current state of the auto scaling configuration\. If the status of the configuration revision is `ACTIVE`, your auto scaling configuration exists\. If the status of a configuration revision is `INACTIVE`, your auto scaling configuration was deleted and can't be used\. Inactive configuration revisions are permanently removed some time after they are deleted\. 

## Examples<a name="aws-resource-apprunner-autoscalingconfiguration--examples"></a>

### Auto Scaling configuration<a name="aws-resource-apprunner-autoscalingconfiguration--examples--Auto_Scaling_configuration"></a>

This example illustrates setting up an automatic scaling configuration for your App Runner service\.

#### JSON<a name="aws-resource-apprunner-autoscalingconfiguration--examples--Auto_Scaling_configuration--json"></a>

```
{
  "Type": "AWS::AppRunner::AutoScalingConfiguration",
  "Properties": {
    "AutoScalingConfigurationName": "AUTO_SCALING_CONFIGURATION_NAME",
    "MaxConcurrency": 100,
    "MaxSize": 25,
    "MinSize": 1
  }
}
```

#### YAML<a name="aws-resource-apprunner-autoscalingconfiguration--examples--Auto_Scaling_configuration--yaml"></a>

```
Type: AWS::AppRunner::AutoScalingConfiguration
Properties:
  AutoScalingConfigurationName: "AUTO_SCALING_CONFIGURATION_NAME"
  MaxConcurrency: 100
  MaxSize: 25
  MinSize: 1
```

## See also<a name="aws-resource-apprunner-autoscalingconfiguration--seealso"></a>
+ [Managing App Runner automatic scaling](https://docs.aws.amazon.com/apprunner/latest/dg/manage-autoscaling.html) in the *AWS App Runner Developer Guide*