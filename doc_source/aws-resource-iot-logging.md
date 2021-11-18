# AWS::IoT::Logging<a name="aws-resource-iot-logging"></a>

Sets the logging options in the V2 logging service\.

## Syntax<a name="aws-resource-iot-logging-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iot-logging-syntax.json"></a>

```
{
  "Type" : "AWS::IoT::Logging",
  "Properties" : {
      "[AccountId](#cfn-iot-logging-accountid)" : String,
      "[DefaultLogLevel](#cfn-iot-logging-defaultloglevel)" : String,
      "[RoleArn](#cfn-iot-logging-rolearn)" : String
    }
}
```

### YAML<a name="aws-resource-iot-logging-syntax.yaml"></a>

```
Type: AWS::IoT::Logging
Properties: 
  [AccountId](#cfn-iot-logging-accountid): String
  [DefaultLogLevel](#cfn-iot-logging-defaultloglevel): String
  [RoleArn](#cfn-iot-logging-rolearn): String
```

## Properties<a name="aws-resource-iot-logging-properties"></a>

`AccountId`  <a name="cfn-iot-logging-accountid"></a>
The unique identifier of the account to use when writing to CloudWatch logs\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DefaultLogLevel`  <a name="cfn-iot-logging-defaultloglevel"></a>
The logging level\. Valid values are `DEBUG`, `INFO`, `ERROR`, `WARN`, and `DISABLED`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-logging-rolearn"></a>
The ARN of the role that allows IoT to write to Cloudwatch logs\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iot-logging-return-values"></a>

### Ref<a name="aws-resource-iot-logging-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns

 `{ "Ref": "AccountId" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.