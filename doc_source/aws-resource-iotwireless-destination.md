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
      "[NextToken](#cfn-iotwireless-destination-nexttoken)" : String,
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
  [NextToken](#cfn-iotwireless-destination-nexttoken): String
  [RoleArn](#cfn-iotwireless-destination-rolearn): String
  [Tags](#cfn-iotwireless-destination-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-iotwireless-destination-properties"></a>

`Description`  <a name="cfn-iotwireless-destination-description"></a>
The description of the new resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-iotwireless-destination-expression"></a>
The rule name to send messages to\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExpressionType`  <a name="cfn-iotwireless-destination-expressiontype"></a>
The type of value in `Expression`\. Must be `RuleName` or `TopicPattern`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotwireless-destination-name"></a>
The name of the new resource\. Can have only have alphanumeric, \- \(hyphen\) and \_ \(underscore\) characters and it can't have any spaces\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NextToken`  <a name="cfn-iotwireless-destination-nexttoken"></a>
This parameter isn't needed to create this resource\. Do not include it in your template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iotwireless-destination-rolearn"></a>
The ARN of the IAM Role that authorizes the destination\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-iotwireless-destination-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iotwireless-destination-return-values"></a>

### Ref<a name="aws-resource-iotwireless-destination-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Destination name\.

### Fn::GetAtt<a name="aws-resource-iotwireless-destination-return-values-fn--getatt"></a>

#### <a name="aws-resource-iotwireless-destination-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the destination created\.