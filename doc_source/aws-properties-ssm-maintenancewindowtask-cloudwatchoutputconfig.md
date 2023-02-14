# AWS::SSM::MaintenanceWindowTask CloudWatchOutputConfig<a name="aws-properties-ssm-maintenancewindowtask-cloudwatchoutputconfig"></a>

Configuration options for sending command output to Amazon CloudWatch Logs\.

## Syntax<a name="aws-properties-ssm-maintenancewindowtask-cloudwatchoutputconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssm-maintenancewindowtask-cloudwatchoutputconfig-syntax.json"></a>

```
{
  "[CloudWatchLogGroupName](#cfn-ssm-maintenancewindowtask-cloudwatchoutputconfig-cloudwatchloggroupname)" : String,
  "[CloudWatchOutputEnabled](#cfn-ssm-maintenancewindowtask-cloudwatchoutputconfig-cloudwatchoutputenabled)" : Boolean
}
```

### YAML<a name="aws-properties-ssm-maintenancewindowtask-cloudwatchoutputconfig-syntax.yaml"></a>

```
  [CloudWatchLogGroupName](#cfn-ssm-maintenancewindowtask-cloudwatchoutputconfig-cloudwatchloggroupname): String
  [CloudWatchOutputEnabled](#cfn-ssm-maintenancewindowtask-cloudwatchoutputconfig-cloudwatchoutputenabled): Boolean
```

## Properties<a name="aws-properties-ssm-maintenancewindowtask-cloudwatchoutputconfig-properties"></a>

`CloudWatchLogGroupName`  <a name="cfn-ssm-maintenancewindowtask-cloudwatchoutputconfig-cloudwatchloggroupname"></a>
The name of the CloudWatch Logs log group where you want to send command output\. If you don't specify a group name, AWS Systems Manager automatically creates a log group for you\. The log group uses the following naming format:  
 `aws/ssm/SystemsManagerDocumentName `   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CloudWatchOutputEnabled`  <a name="cfn-ssm-maintenancewindowtask-cloudwatchoutputconfig-cloudwatchoutputenabled"></a>
Enables Systems Manager to send command output to CloudWatch Logs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)