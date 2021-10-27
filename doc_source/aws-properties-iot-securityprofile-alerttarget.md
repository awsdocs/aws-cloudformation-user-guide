# AWS::IoT::SecurityProfile AlertTarget<a name="aws-properties-iot-securityprofile-alerttarget"></a>

A structure containing the alert target ARN and the role ARN\.

## Syntax<a name="aws-properties-iot-securityprofile-alerttarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-securityprofile-alerttarget-syntax.json"></a>

```
{
  "[AlertTargetArn](#cfn-iot-securityprofile-alerttarget-alerttargetarn)" : String,
  "[RoleArn](#cfn-iot-securityprofile-alerttarget-rolearn)" : String
}
```

### YAML<a name="aws-properties-iot-securityprofile-alerttarget-syntax.yaml"></a>

```
  [AlertTargetArn](#cfn-iot-securityprofile-alerttarget-alerttargetarn): String
  [RoleArn](#cfn-iot-securityprofile-alerttarget-rolearn): String
```

## Properties<a name="aws-properties-iot-securityprofile-alerttarget-properties"></a>

`AlertTargetArn`  <a name="cfn-iot-securityprofile-alerttarget-alerttargetarn"></a>
The Amazon Resource Name \(ARN\) of the notification target to which alerts are sent\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-iot-securityprofile-alerttarget-rolearn"></a>
The ARN of the role that grants permission to send alerts to the notification target\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)