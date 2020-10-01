# AWS::DMS::Endpoint KinesisSettings<a name="aws-properties-dms-endpoint-kinesissettings"></a>

Provides information that describes an Amazon Kinesis Data Stream endpoint\. This information includes the output format of records applied to the endpoint and details of transaction and control table data information\.

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
The output format for the records created on the endpoint\. The message format is `JSON` \(default\) or `JSON_UNFORMATTED` \(a single line with no tab\)\.  
*Required*: No  
*Type*: String  
*Allowed values*: `json | json-unformatted`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceAccessRoleArn`  <a name="cfn-dms-endpoint-kinesissettings-serviceaccessrolearn"></a>
The Amazon Resource Name \(ARN\) for the AWS Identity and Access Management \(IAM\) role that AWS DMS uses to write to the Kinesis data stream\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StreamArn`  <a name="cfn-dms-endpoint-kinesissettings-streamarn"></a>
The Amazon Resource Name \(ARN\) for the Amazon Kinesis Data Streams endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)