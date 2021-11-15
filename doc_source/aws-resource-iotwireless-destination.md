# AWS::IoTWireless::Destination<a name="aws-resource-iotwireless-destination"></a>

Creates a new destination that maps a device message to an AWS IoT rule\.

## Syntax<a name="aws-resource-iotwireless-destination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iotwireless-destination-syntax.json"></a>

```
{
  "Type" : "AWS::IoTWireless::Destination",
  "Properties" : {
      "[Description](#cfn-iotwireless-destination-description)" : String,
      "[Expression](#cfn-iotwireless-destination-expression)" : String,
      "[ExpressionType](#cfn-iotwireless-destination-expressiontype)" : String,
      "[Name](#cfn-iotwireless-destination-name)" : String,
      "[RoleArn](#cfn-iotwireless-destination-rolearn)" : String,
      "[Tags](#cfn-iotwireless-destination-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-iotwireless-destination-syntax.yaml"></a>

```
Type: AWS::IoTWireless::Destination
Properties: 
  [Description](#cfn-iotwireless-destination-description): String
  [Expression](#cfn-iotwireless-destination-expression): String
  [ExpressionType](#cfn-iotwireless-destination-expressiontype): String
  [Name](#cfn-iotwireless-destination-name): String
  [RoleArn](#cfn-iotwireless-destination-rolearn): String
  [Tags](#cfn-iotwireless-destination-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotwireless-destination-properties"></a>

`Description`  <a name="cfn-iotwireless-destination-description"></a>
The description of the new resource\. Maximum length is 2048 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-iotwireless-destination-expression"></a>
The rule name to send messages to\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExpressionType`  <a name="cfn-iotwireless-destination-expressiontype"></a>
The type of value in `Expression`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `MqttTopic | RuleName`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotwireless-destination-name"></a>
The name of the new resource\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9-_]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-iotwireless-destination-rolearn"></a>
The ARN of the IAM Role that authorizes the destination\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-destination-tags"></a>
The tags are an array of key\-value pairs to attach to the specified resource\. Tags can have a minimum of 0 and a maximum of 50 items\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotwireless-destination-return-values"></a>

### Ref<a name="aws-resource-iotwireless-destination-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Destination name\.

### Fn::GetAtt<a name="aws-resource-iotwireless-destination-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotwireless-destination-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the destination created\.