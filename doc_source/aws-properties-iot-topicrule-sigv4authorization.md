# AWS::IoT::TopicRule SigV4Authorization<a name="aws-properties-iot-topicrule-sigv4authorization"></a>

Use Sig V4 authorization\.

## Syntax<a name="aws-properties-iot-topicrule-sigv4authorization-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-topicrule-sigv4authorization-syntax.json"></a>

```
{
  "[RoleArn](#cfn-iot-topicrule-sigv4authorization-rolearn)" : String,
  "[ServiceName](#cfn-iot-topicrule-sigv4authorization-servicename)" : String,
  "[SigningRegion](#cfn-iot-topicrule-sigv4authorization-signingregion)" : String
}
```

### YAML<a name="aws-properties-iot-topicrule-sigv4authorization-syntax.yaml"></a>

```
  [RoleArn](#cfn-iot-topicrule-sigv4authorization-rolearn): String
  [ServiceName](#cfn-iot-topicrule-sigv4authorization-servicename): String
  [SigningRegion](#cfn-iot-topicrule-sigv4authorization-signingregion): String
```

## Properties<a name="aws-properties-iot-topicrule-sigv4authorization-properties"></a>

`RoleArn`  <a name="cfn-iot-topicrule-sigv4authorization-rolearn"></a>
The ARN of the signing role\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceName`  <a name="cfn-iot-topicrule-sigv4authorization-servicename"></a>
The service name to use while signing with Sig V4\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SigningRegion`  <a name="cfn-iot-topicrule-sigv4authorization-signingregion"></a>
The signing region\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)