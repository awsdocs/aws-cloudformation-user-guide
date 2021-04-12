# AWS::ECS::Cluster ExecuteCommandConfiguration<a name="aws-properties-ecs-cluster-executecommandconfiguration"></a>

The details of the execute command configuration\.

## Syntax<a name="aws-properties-ecs-cluster-executecommandconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecs-cluster-executecommandconfiguration-syntax.json"></a>

```
{
  "[KmsKeyId](#cfn-ecs-cluster-executecommandconfiguration-kmskeyid)" : String,
  "[LogConfiguration](#cfn-ecs-cluster-executecommandconfiguration-logconfiguration)" : ExecuteCommandLogConfiguration,
  "[Logging](#cfn-ecs-cluster-executecommandconfiguration-logging)" : String
}
```

### YAML<a name="aws-properties-ecs-cluster-executecommandconfiguration-syntax.yaml"></a>

```
  [KmsKeyId](#cfn-ecs-cluster-executecommandconfiguration-kmskeyid): String
  [LogConfiguration](#cfn-ecs-cluster-executecommandconfiguration-logconfiguration): 
    ExecuteCommandLogConfiguration
  [Logging](#cfn-ecs-cluster-executecommandconfiguration-logging): String
```

## Properties<a name="aws-properties-ecs-cluster-executecommandconfiguration-properties"></a>

`KmsKeyId`  <a name="cfn-ecs-cluster-executecommandconfiguration-kmskeyid"></a>
Specify an AWS Key Management Service key ID to encrypt the data between the local client and the container\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogConfiguration`  <a name="cfn-ecs-cluster-executecommandconfiguration-logconfiguration"></a>
The log configuration for the results of the execute command actions\. The logs can be sent to CloudWatch Logs or an Amazon S3 bucket\. When `logging=OVERRIDE` is specified, a `logConfiguration` must be provided\.  
*Required*: No  
*Type*: [ExecuteCommandLogConfiguration](aws-properties-ecs-cluster-executecommandlogconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Logging`  <a name="cfn-ecs-cluster-executecommandconfiguration-logging"></a>
The log setting to use for redirecting logs for your execute command results\. The following log settings are available\.  
+  `NONE`: The execute command session is not logged\.
+  `DEFAULT`: The `awslogs` configuration in the task definition is used\. If no logging parameter is specified, it defaults to this value\. If no `awslogs` log driver is configured in the task definition, the output won't be logged\.
+  `OVERRIDE`: Specify the logging details as a part of `logConfiguration`\. If the `OVERRIDE` logging option is specified, the `logConfiguration` is required\.
*Required*: No  
*Type*: String  
*Allowed values*: `DEFAULT | NONE | OVERRIDE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)