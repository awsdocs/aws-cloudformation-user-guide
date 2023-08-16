# AWS::IoT::Dimension<a name="aws-resource-iot-dimension"></a>

Use the `AWS::IoT::Dimension` to limit the scope of a metric used in a security profile for AWS IoT Device Defender\. For example, using a `TOPIC_FILTER` dimension, you can narrow down the scope of the metric to only MQTT topics where the name matches the pattern specified in the dimension\. For API reference, see [CreateDimension](https://docs.aws.amazon.com/iot/latest/apireference/API_CreateDimension.html) and for general information, see [Scoping metrics in security profiles using dimensions](https://docs.aws.amazon.com/iot/latest/developerguide/scoping-security-behavior.html)\.

## Syntax<a name="aws-resource-iot-dimension-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-dimension-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::Dimension",
  "Properties" : {
      "[Name](#cfn-iot-dimension-name)" : String,
      "[StringValues](#cfn-iot-dimension-stringvalues)" : [ String, ... ],
      "[Tags](#cfn-iot-dimension-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-iot-dimension-type)" : String
    }
}
```

### YAML<a name="aws-resource-iot-dimension-syntax.yaml"></a>

```
Type: AWS::IoT::Dimension
Properties: 
  [Name](#cfn-iot-dimension-name): String
  [StringValues](#cfn-iot-dimension-stringvalues): 
    - String
  [Tags](#cfn-iot-dimension-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-iot-dimension-type): String
```

## Properties<a name="aws-resource-iot-dimension-properties"></a>

`Name`  <a name="cfn-iot-dimension-name"></a>
A unique identifier for the dimension\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StringValues`  <a name="cfn-iot-dimension-stringvalues"></a>
Specifies the value or list of values for the dimension\. For `TOPIC_FILTER` dimensions, this is a pattern used to match the MQTT topic \(for example, "admin/\#"\)\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iot-dimension-tags"></a>
Metadata that can be used to manage the dimension\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-iot-dimension-type"></a>
Specifies the type of dimension\. Supported types: `TOPIC_FILTER.`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-iot-dimension-return-values"></a>

### Ref<a name="aws-resource-iot-dimension-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the dimension name\.

### Fn::GetAtt<a name="aws-resource-iot-dimension-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-iot-dimension-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the dimension\.

## Examples<a name="aws-resource-iot-dimension--examples"></a>



### <a name="aws-resource-iot-dimension--examples--"></a>



#### JSON<a name="aws-resource-iot-dimension--examples----json"></a>

```
{ "AWSTemplateFormatVersion": "2010-09-09", "Description": "Amazon
            Web Services IoT Dimension Sample Template", "Resources": {
            "TopicFilterForAuthMessagesDimension": { "Type": "AWS::IoT::Dimension", "Properties": {
            "Name": "TopicFilterForAuthMessages", "Type": "TOPIC_FILTER", "StringValues": [
            "device/+/auth" ], "Tags": [ { "Key": "Application", "Value": "SmartHome" } ] } } }
            }
```

#### YAML<a name="aws-resource-iot-dimension--examples----yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09 Description: Amazon Web
            Services IoT Dimension Sample Template Resources: TopicFilterForAuthMessagesDimension:
            Type: 'AWS::IoT::Dimension' Properties: Name: TopicFilterForAuthMessages Type:
            TOPIC_FILTER StringValues: - device/+/auth Tags: - Key: Application Value:
            SmartHome
```