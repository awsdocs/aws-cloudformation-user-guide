# AWS::Greengrass::FunctionDefinitionVersion ResourceAccessPolicy<a name="aws-properties-greengrass-functiondefinitionversion-resourceaccesspolicy"></a>

<a name="aws-properties-greengrass-functiondefinitionversion-resourceaccesspolicy-description"></a>A list of the [resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinitionversion-resourceinstance.html) in the group that the function can access, with the corresponding read\-only or read\-write permissions\. The maximum is 10 resources\.

**Note**  
This property applies only to Lambda functions that run in a Greengrass container\.

<a name="aws-properties-greengrass-functiondefinitionversion-resourceaccesspolicy-inheritance"></a> In an AWS CloudFormation template, `ResourceAccessPolicy` is a property of the [ `Environment` ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-functiondefinitionversion-environment.html) property type\.

## Syntax<a name="aws-properties-greengrass-functiondefinitionversion-resourceaccesspolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-functiondefinitionversion-resourceaccesspolicy-syntax.json"></a>

```
{
  "[Permission](#cfn-greengrass-functiondefinitionversion-resourceaccesspolicy-permission)" : String,
  "[ResourceId](#cfn-greengrass-functiondefinitionversion-resourceaccesspolicy-resourceid)" : String
}
```

### YAML<a name="aws-properties-greengrass-functiondefinitionversion-resourceaccesspolicy-syntax.yaml"></a>

```
  [Permission](#cfn-greengrass-functiondefinitionversion-resourceaccesspolicy-permission): String
  [ResourceId](#cfn-greengrass-functiondefinitionversion-resourceaccesspolicy-resourceid): String
```

## Properties<a name="aws-properties-greengrass-functiondefinitionversion-resourceaccesspolicy-properties"></a>

`Permission`  <a name="cfn-greengrass-functiondefinitionversion-resourceaccesspolicy-permission"></a>
The read\-only or read\-write access that the Lambda function has to the resource\. Valid values are `ro` or `rw`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceId`  <a name="cfn-greengrass-functiondefinitionversion-resourceaccesspolicy-resourceid"></a>
The ID of the resource\. This ID is assigned to the resource when you create the resource definition\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## See also<a name="aws-properties-greengrass-functiondefinitionversion-resourceaccesspolicy--seealso"></a>
+  [ResourceAccessPolicy](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-resourceaccesspolicy.html) in the * AWS IoT Greengrass API Reference * 
+  [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/) 