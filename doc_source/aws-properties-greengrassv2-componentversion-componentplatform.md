# AWS::GreengrassV2::ComponentVersion ComponentPlatform<a name="aws-properties-greengrassv2-componentversion-componentplatform"></a>

Contains information about a platform that a component supports\.

## Syntax<a name="aws-properties-greengrassv2-componentversion-componentplatform-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-greengrassv2-componentversion-componentplatform-syntax.json"></a>

```
{
  "[Attributes](#cfn-greengrassv2-componentversion-componentplatform-attributes)" : {Key : Value, ...},
  "[Name](#cfn-greengrassv2-componentversion-componentplatform-name)" : String
}
```

### YAML<a name="aws-properties-greengrassv2-componentversion-componentplatform-syntax.yaml"></a>

```
  [Attributes](#cfn-greengrassv2-componentversion-componentplatform-attributes): 
    Key : Value
  [Name](#cfn-greengrassv2-componentversion-componentplatform-name): String
```

## Properties<a name="aws-properties-greengrassv2-componentversion-componentplatform-properties"></a>

`Attributes`  <a name="cfn-greengrassv2-componentversion-componentplatform-attributes"></a>
A dictionary of attributes for the platform\. The AWS IoT Greengrass Core software defines the `os` and `platform` by default\. You can specify additional platform attributes for a core device when you deploy the Greengrass nucleus component\. For more information, see the [Greengrass nucleus component](https://docs.aws.amazon.com/greengrass/v2/developerguide/greengrass-nucleus-component.html) in the *AWS IoT Greengrass V2 Developer Guide*\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-greengrassv2-componentversion-componentplatform-name"></a>
The friendly name of the platform\. This name helps you identify the platform\.  
If you omit this parameter, AWS IoT Greengrass creates a friendly name from the `os` and `architecture` of the platform\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)