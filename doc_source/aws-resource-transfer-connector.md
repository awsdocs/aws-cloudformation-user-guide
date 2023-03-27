# AWS::Transfer::Connector<a name="aws-resource-transfer-connector"></a>

Creates the connector, which captures the parameters for an outbound connection for the AS2 protocol\. The connector is required for sending files to an externally hosted AS2 server\. For more details about connectors, see [Create AS2 connectors](https://docs.aws.amazon.com/transfer/latest/userguide/create-b2b-server.html#configure-as2-connector)\.

## Syntax<a name="aws-resource-transfer-connector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-transfer-connector-syntax.json"></a>

```
{
  "Type" : "AWS::Transfer::Connector",
  "Properties" : {
      "[AccessRole](#cfn-transfer-connector-accessrole)" : String,
      "[As2Config](#cfn-transfer-connector-as2config)" : As2Config,
      "[LoggingRole](#cfn-transfer-connector-loggingrole)" : String,
      "[Tags](#cfn-transfer-connector-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Url](#cfn-transfer-connector-url)" : String
    }
}
```

### YAML<a name="aws-resource-transfer-connector-syntax.yaml"></a>

```
Type: AWS::Transfer::Connector
Properties: 
  [AccessRole](#cfn-transfer-connector-accessrole): String
  [As2Config](#cfn-transfer-connector-as2config): 
    As2Config
  [LoggingRole](#cfn-transfer-connector-loggingrole): String
  [Tags](#cfn-transfer-connector-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Url](#cfn-transfer-connector-url): String
```

## Properties<a name="aws-resource-transfer-connector-properties"></a>

`AccessRole`  <a name="cfn-transfer-connector-accessrole"></a>
With AS2, you can send files by calling `StartFileTransfer` and specifying the file paths in the request parameter, `SendFilePaths`\. We use the file’s parent directory \(for example, for `--send-file-paths /bucket/dir/file.txt`, parent directory is `/bucket/dir/`\) to temporarily store a processed AS2 message file, store the MDN when we receive them from the partner, and write a final JSON file containing relevant metadata of the transmission\. So, the `AccessRole` needs to provide read and write access to the parent directory of the file location used in the `StartFileTransfer` request\. Additionally, you need to provide read and write access to the parent directory of the files that you intend to send with `StartFileTransfer`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:.*role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`As2Config`  <a name="cfn-transfer-connector-as2config"></a>
A structure that contains the parameters for a connector object\.  
*Required*: Yes  
*Type*: [As2Config](aws-properties-transfer-connector-as2config.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingRole`  <a name="cfn-transfer-connector-loggingrole"></a>
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) role that allows a connector to turn on CloudWatch logging for Amazon S3 events\. When set, you can view connector activity in your CloudWatch logs\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:.*role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-transfer-connector-tags"></a>
Key\-value pairs that can be used to group and search for connectors\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Url`  <a name="cfn-transfer-connector-url"></a>
The URL of the partner's AS2 endpoint\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-transfer-connector-return-values"></a>

### Ref<a name="aws-resource-transfer-connector-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-transfer-connector-return-values-fn--getatt"></a>

#### <a name="aws-resource-transfer-connector-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.

`ConnectorId`  <a name="ConnectorId-fn::getatt"></a>
Property description not available\.