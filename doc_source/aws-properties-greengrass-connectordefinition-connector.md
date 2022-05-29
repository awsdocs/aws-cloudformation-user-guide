# AWS::Greengrass::ConnectorDefinition Connector<a name="aws-properties-greengrass-connectordefinition-connector"></a>

<a name="aws-properties-greengrass-connectordefinition-connector-description"></a>Connectors are modules that provide built\-in integration with local infrastructure, device protocols, AWS, and other cloud services\. For more information, see [Integrate with Services and Protocols Using Greengrass Connectors](https://docs.aws.amazon.com/greengrass/latest/developerguide/connectors.html) in the *AWS IoT Greengrass Version 1 Developer Guide*\.

<a name="aws-properties-greengrass-connectordefinitionversion-connector-inheritance"></a> In an AWS CloudFormation template, the `Connectors` property of the [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-connectordefinition-connectordefinitionversion.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-connectordefinition-connectordefinitionversion.html) property type contains a list of `Connector` property types\.

## Syntax<a name="aws-properties-greengrass-connectordefinition-connector-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-connectordefinition-connector-syntax.json"></a>

```
{
  "[ConnectorArn](#cfn-greengrass-connectordefinition-connector-connectorarn)" : String,
  "[Id](#cfn-greengrass-connectordefinition-connector-id)" : String,
  "[Parameters](#cfn-greengrass-connectordefinition-connector-parameters)" : Json
}
```

### YAML<a name="aws-properties-greengrass-connectordefinition-connector-syntax.yaml"></a>

```
  [ConnectorArn](#cfn-greengrass-connectordefinition-connector-connectorarn): String
  [Id](#cfn-greengrass-connectordefinition-connector-id): String
  [Parameters](#cfn-greengrass-connectordefinition-connector-parameters): Json
```

## Properties<a name="aws-properties-greengrass-connectordefinition-connector-properties"></a>

`ConnectorArn`  <a name="cfn-greengrass-connectordefinition-connector-connectorarn"></a>
The Amazon Resource Name \(ARN\) of the connector\.  
For more information about connectors provided by AWS, see [Greengrass Connectors Provided by AWS](https://docs.aws.amazon.com/greengrass/latest/developerguide/connectors-list.html)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Id`  <a name="cfn-greengrass-connectordefinition-connector-id"></a>
A descriptive or arbitrary ID for the connector\. This value must be unique within the connector definition version\. Maximum length is 128 characters with pattern `[a-zA-Z0-9:_-]+`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Parameters`  <a name="cfn-greengrass-connectordefinition-connector-parameters"></a>
The parameters or configuration used by the connector\.  
For more information about connectors provided by AWS, see [Greengrass Connectors Provided by AWS](https://docs.aws.amazon.com/greengrass/latest/developerguide/connectors-list.html)\.  
*Required*: No  
*Type*: Json  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-connectordefinition-connector--seealso"></a>
+  [Connector](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-connector.html) in the * AWS IoT Greengrass Version 1 API Reference * 
+  [AWS IoT Greengrass Version 1 Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 