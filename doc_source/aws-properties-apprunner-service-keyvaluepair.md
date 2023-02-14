# AWS::AppRunner::Service KeyValuePair<a name="aws-properties-apprunner-service-keyvaluepair"></a>

Describes a key\-value pair, which is a string\-to\-string mapping\.

## Syntax<a name="aws-properties-apprunner-service-keyvaluepair-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-keyvaluepair-syntax.json"></a>

```
{
  "[Name](#cfn-apprunner-service-keyvaluepair-name)" : String,
  "[Value](#cfn-apprunner-service-keyvaluepair-value)" : String
}
```

### YAML<a name="aws-properties-apprunner-service-keyvaluepair-syntax.yaml"></a>

```
  [Name](#cfn-apprunner-service-keyvaluepair-name): String
  [Value](#cfn-apprunner-service-keyvaluepair-value): String
```

## Properties<a name="aws-properties-apprunner-service-keyvaluepair-properties"></a>

`Name`  <a name="cfn-apprunner-service-keyvaluepair-name"></a>
The key name string to map to a value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-apprunner-service-keyvaluepair-value"></a>
The value string to which the key name is mapped\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)