# AWS IoT Greengrass FunctionDefinition ResourceAccessPolicy<a name="aws-properties-greengrass-functiondefinition-resourceaccesspolicy"></a>

<a name="aws-properties-greengrass-functiondefinition-resourceaccesspolicy-description"></a>A list of the [resources](aws-properties-greengrass-resourcedefinitionversion-resourceinstance.md) in the group that the function can access, with the corresponding read\-only or read\-write permissions\. The maximum is 10 resources\.

**Note**  
This property applies only to Lambda functions that run in a Greengrass container\.

<a name="aws-properties-greengrass-functiondefinition-resourceaccesspolicy-inheritance"></a> In an AWS CloudFormation template, `ResourceAccessPolicy` is a property of the [Environment](aws-properties-greengrass-functiondefinition-environment.md) property type\.

## Syntax<a name="aws-properties-greengrass-functiondefinition-resourceaccesspolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrass-functiondefinition-resourceaccesspolicy-syntax.json"></a>

```
{
  "[ResourceId](#cfn-greengrass-functiondefinition-resourceaccesspolicy-resourceid)" : String,
  "[Permission](#cfn-greengrass-functiondefinition-resourceaccesspolicy-permission)" : String
}
```

### YAML<a name="aws-properties-greengrass-functiondefinition-resourceaccesspolicy-syntax.yaml"></a>

```
[ResourceId](#cfn-greengrass-functiondefinition-resourceaccesspolicy-resourceid): String
[Permission](#cfn-greengrass-functiondefinition-resourceaccesspolicy-permission): String
```

## Properties<a name="aws-properties-greengrass-functiondefinition-resourceaccesspolicy-properties"></a>

`ResourceId`  <a name="cfn-greengrass-functiondefinition-resourceaccesspolicy-resourceid"></a>
The ID of the resource\. This ID is assigned to the resource when you create the resource definiton\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Permission`  <a name="cfn-greengrass-functiondefinition-resourceaccesspolicy-permission"></a>
The read\-only or read\-write access that the Lambda function has to the resource\. Valid values are `ro` or `rw`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## See Also<a name="aws-properties-greengrass-functiondefinition-resourceaccesspolicy-seealso"></a>
+ [ResourceAccessPolicy](https://docs.aws.amazon.com/greengrass/latest/apireference/definitions-resourceaccesspolicy.html) in the *AWS IoT Greengrass API Reference*
+ [AWS IoT Greengrass Developer Guide](https://docs.aws.amazon.com/greengrass/latest/developerguide/)