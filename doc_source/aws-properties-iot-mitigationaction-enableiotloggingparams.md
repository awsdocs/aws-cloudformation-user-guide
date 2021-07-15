# AWS::IoT::MitigationAction EnableIoTLoggingParams<a name="aws-properties-iot-mitigationaction-enableiotloggingparams"></a>

Parameters used when defining a mitigation action that enable AWS IoT Core logging\.

## Syntax<a name="aws-properties-iot-mitigationaction-enableiotloggingparams-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iot-mitigationaction-enableiotloggingparams-syntax.json"></a>

```
{
  "[LogLevel](#cfn-iot-mitigationaction-enableiotloggingparams-loglevel)" : String,
  "[RoleArnForLogging](#cfn-iot-mitigationaction-enableiotloggingparams-rolearnforlogging)" : String
}
```

### YAML<a name="aws-properties-iot-mitigationaction-enableiotloggingparams-syntax.yaml"></a>

```
  [LogLevel](#cfn-iot-mitigationaction-enableiotloggingparams-loglevel): String
  [RoleArnForLogging](#cfn-iot-mitigationaction-enableiotloggingparams-rolearnforlogging): String
```

## Properties<a name="aws-properties-iot-mitigationaction-enableiotloggingparams-properties"></a>

`LogLevel`  <a name="cfn-iot-mitigationaction-enableiotloggingparams-loglevel"></a>
Specifies the type of information to be logged\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArnForLogging`  <a name="cfn-iot-mitigationaction-enableiotloggingparams-rolearnforlogging"></a>
The Amazon Resource Name \(ARN\) of the IAM role used for logging\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)