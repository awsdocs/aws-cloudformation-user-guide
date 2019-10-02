# AWS::DMS::Endpoint KinesisSettings<a name="aws-properties-dms-endpoint-kinesissettings"></a>

## Syntax<a name="aws-properties-dms-endpoint-kinesissettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-endpoint-kinesissettings-syntax.json"></a>

```
{
  "[MessageFormat](#cfn-dms-endpoint-kinesissettings-messageformat)" : String,
  "[ServiceAccessRoleArn](#cfn-dms-endpoint-kinesissettings-serviceaccessrolearn)" : String,
  "[StreamArn](#cfn-dms-endpoint-kinesissettings-streamarn)" : String
}
```

### YAML<a name="aws-properties-dms-endpoint-kinesissettings-syntax.yaml"></a>

```
  [MessageFormat](#cfn-dms-endpoint-kinesissettings-messageformat): String
  [ServiceAccessRoleArn](#cfn-dms-endpoint-kinesissettings-serviceaccessrolearn): String
  [StreamArn](#cfn-dms-endpoint-kinesissettings-streamarn): String
```

## Properties<a name="aws-properties-dms-endpoint-kinesissettings-properties"></a>

`MessageFormat`  <a name="cfn-dms-endpoint-kinesissettings-messageformat"></a>
The output format for the records created on the endpoint\. The message format is `JSON`\.  
*Required*: No  
*Type*: String  
*Allowed Values*: `json`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccessRoleArn`  <a name="cfn-dms-endpoint-kinesissettings-serviceaccessrolearn"></a>
The Amazon Resource Name \(ARN\) for the IAM role that DMS uses to write to the Amazon Kinesis data stream\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamArn`  <a name="cfn-dms-endpoint-kinesissettings-streamarn"></a>
The Amazon Resource Name \(ARN\) for the Amazon Kinesis Data Streams endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `cn-north-1`
- `cn-northwest-1`
- `eu-central-1`
- `eu-north-1`
- `eu-west-1`
- `eu-west-2`
- `sa-east-1`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
