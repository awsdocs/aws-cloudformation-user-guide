# AWS IoT Greengrass FunctionDefinitionVersion RunAs<a name="aws-properties-greengrass-functiondefinitionversion-runas"></a>

<a name="aws-properties-greengrass-functiondefinitionversion-runas-description"></a>The user and group permissions used to run the Lambda function\. This setting overrides the default access identity that's specified for the group \(by default, ggc\_user and ggc\_group\)\. You can override the user, group, or both\. For more information, see [Run as](https://docs.aws.amazon.com/greengrass/latest/developerguide/lambda-group-config.html#lambda-access-identity.html) in the *AWS IoT Greengrass Developer Guide*\.

**Important**  
Running as the root user increases risks to your data and device\. Do not run as root \(UID/GID=0\) unless your business case requires it\. For more information and requirements, see [Running a Lambda Function as Root](https://docs.aws.amazon.com/greengrass/latest/developerguide/lambda-group-config.html#lambda-running-as-root)\. 

<a name="aws-properties-greengrass-functiondefinitionversion-runas-inheritance"></a> In an AWS CloudFormation template, `RunAs` is a property of the [Execution](aws-properties-greengrass-functiondefinitionversion-execution.md) property type\.

## Syntax<a name="aws-properties-greengrass-functiondefinitionversion-runas-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-functiondefinitionversion-runas-syntax.json"></a>

```
{
  "[Uid](#cfn-greengrass-functiondefinitionversion-runas-uid)" : Integer,
  "[Gid](#cfn-greengrass-functiondefinitionversion-runas-gid)" : Integer
}
```

### YAML<a name="aws-properties-greengrass-functiondefinitionversion-runas-syntax.yaml"></a>

```
[Uid](#cfn-greengrass-functiondefinitionversion-runas-uid): Integer
[Gid](#cfn-greengrass-functiondefinitionversion-runas-gid): Integer
```

## Properties<a name="aws-properties-greengrass-functiondefinitionversion-runas-properties"></a>

`Uid`  <a name="cfn-greengrass-functiondefinitionversion-runas-uid"></a>
The user ID whose permissions are used to run the Lambda function\. You can use the getent passwd command on your core device to look up the user ID\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Gid`  <a name="cfn-greengrass-functiondefinitionversion-runas-gid"></a>
The group ID whose permissions are used to run the Lambda function\. You can use the getent group command on your core device to look up the group ID\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-functiondefinitionversion-runas-seealso"></a>
+ [FunctionExecutionConfig](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-functionexecutionconfig.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)