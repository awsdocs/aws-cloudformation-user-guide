# AWS::Greengrass::FunctionDefinition RunAs<a name="aws-properties-greengrass-functiondefinition-runas"></a>

<a name="aws-properties-greengrass-functiondefinition-runas-description"></a>The access identity whose permissions are used to run the Lambda function\. This setting overrides the default access identity that's specified for the group \(by default, ggc\_user and ggc\_group\)\. You can override the user, group, or both\. For more information, see [Run as](https://docs.aws.amazon.com/greengrass/latest/developerguide/lambda-group-config.html#lambda-access-identity.html) in the *AWS IoT Greengrass Developer Guide*\.

**Important**  
Running as the root user increases risks to your data and device\. Do not run as root \(UID/GID=0\) unless your business case requires it\. For more information and requirements, see [Running a Lambda Function as Root](https://docs.aws.amazon.com/greengrass/latest/developerguide/lambda-group-config.html#lambda-running-as-root)\. 

<a name="aws-properties-greengrass-functiondefinition-runas-inheritance"></a> In an AWS CloudFormation template, `RunAs` is a property of the [ `Execution` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinition-execution.html) property type\.

## Syntax<a name="aws-properties-greengrass-functiondefinition-runas-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-functiondefinition-runas-syntax.json"></a>

```
{
  "[Gid](#cfn-greengrass-functiondefinition-runas-gid)" : Integer,
  "[Uid](#cfn-greengrass-functiondefinition-runas-uid)" : Integer
}
```

### YAML<a name="aws-properties-greengrass-functiondefinition-runas-syntax.yaml"></a>

```
  [Gid](#cfn-greengrass-functiondefinition-runas-gid): Integer
  [Uid](#cfn-greengrass-functiondefinition-runas-uid): Integer
```

## Properties<a name="aws-properties-greengrass-functiondefinition-runas-properties"></a>

`Gid`  <a name="cfn-greengrass-functiondefinition-runas-gid"></a>
The group ID whose permissions are used to run the Lambda function\. You can use the getent group command on your core device to look up the group ID\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Uid`  <a name="cfn-greengrass-functiondefinition-runas-uid"></a>
The user ID whose permissions are used to run the Lambda function\. You can use the getent passwd command on your core device to look up the user ID\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-functiondefinition-runas--seealso"></a>
+  [FunctionRunAsConfig](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-functionrunasconfig.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 