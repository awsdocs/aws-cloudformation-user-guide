# AWS::AppRunner::Service InstanceConfiguration<a name="aws-properties-apprunner-service-instanceconfiguration"></a>

Describes the runtime configuration of an AWS App Runner service instance \(scaling unit\)\.

## Syntax<a name="aws-properties-apprunner-service-instanceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-instanceconfiguration-syntax.json"></a>

```
{
  "[Cpu](#cfn-apprunner-service-instanceconfiguration-cpu)" : String,
  "[InstanceRoleArn](#cfn-apprunner-service-instanceconfiguration-instancerolearn)" : String,
  "[Memory](#cfn-apprunner-service-instanceconfiguration-memory)" : String
}
```

### YAML<a name="aws-properties-apprunner-service-instanceconfiguration-syntax.yaml"></a>

```
  [Cpu](#cfn-apprunner-service-instanceconfiguration-cpu): String
  [InstanceRoleArn](#cfn-apprunner-service-instanceconfiguration-instancerolearn): String
  [Memory](#cfn-apprunner-service-instanceconfiguration-memory): String
```

## Properties<a name="aws-properties-apprunner-service-instanceconfiguration-properties"></a>

`Cpu`  <a name="cfn-apprunner-service-instanceconfiguration-cpu"></a>
The number of CPU units reserved for each instance of your App Runner service\.  
Default: `1 vCPU`   
*Required*: No  
*Type*: String  
*Minimum*: `4`  
*Maximum*: `6`  
*Pattern*: `1024|2048|(1|2) vCPU`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceRoleArn`  <a name="cfn-apprunner-service-instanceconfiguration-instancerolearn"></a>
The Amazon Resource Name \(ARN\) of an IAM role that provides permissions to your App Runner service\. These are permissions that your code needs when it calls any AWS APIs\.  
*Required*: No  
*Type*: String  
*Minimum*: `29`  
*Maximum*: `1024`  
*Pattern*: `arn:(aws|aws-us-gov|aws-cn|aws-iso|aws-iso-b):iam::[0-9]{12}:(role|role\/service-role)\/[\w+=,.@\-/]{1,1000}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Memory`  <a name="cfn-apprunner-service-instanceconfiguration-memory"></a>
The amount of memory, in MB or GB, reserved for each instance of your App Runner service\.  
Default: `2 GB`   
*Required*: No  
*Type*: String  
*Minimum*: `4`  
*Maximum*: `4`  
*Pattern*: `2048|3072|4096|(2|3|4) GB`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)