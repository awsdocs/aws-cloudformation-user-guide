# AWS::IoTAnalytics::Pipeline AddAttributes<a name="aws-properties-iotanalytics-pipeline-addattributes"></a>

An activity that adds other attributes based on existing attributes in the message\.

## Syntax<a name="aws-properties-iotanalytics-pipeline-addattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-pipeline-addattributes-syntax.json"></a>

```
{
  "[Attributes](#cfn-iotanalytics-pipeline-addattributes-attributes)" : Json,
  "[Name](#cfn-iotanalytics-pipeline-addattributes-name)" : String,
  "[Next](#cfn-iotanalytics-pipeline-addattributes-next)" : String
}
```

### YAML<a name="aws-properties-iotanalytics-pipeline-addattributes-syntax.yaml"></a>

```
  [Attributes](#cfn-iotanalytics-pipeline-addattributes-attributes): Json
  [Name](#cfn-iotanalytics-pipeline-addattributes-name): String
  [Next](#cfn-iotanalytics-pipeline-addattributes-next): String
```

## Properties<a name="aws-properties-iotanalytics-pipeline-addattributes-properties"></a>

`Attributes`  <a name="cfn-iotanalytics-pipeline-addattributes-attributes"></a>
A list of 1\-50 "AttributeNameMapping" objects that map an existing attribute to a new attribute\.  
The existing attributes remain in the message, so if you want to remove the originals, use "RemoveAttributeActivity"\.
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-iotanalytics-pipeline-addattributes-name"></a>
The name of the 'addAttributes' activity\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Next`  <a name="cfn-iotanalytics-pipeline-addattributes-next"></a>
The next activity in the pipeline\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)