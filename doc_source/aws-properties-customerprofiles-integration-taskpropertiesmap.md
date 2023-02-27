# AWS::CustomerProfiles::Integration TaskPropertiesMap<a name="aws-properties-customerprofiles-integration-taskpropertiesmap"></a>

A map used to store task\-related information\. The execution service looks for particular information based on the `TaskType`\.

## Syntax<a name="aws-properties-customerprofiles-integration-taskpropertiesmap-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-integration-taskpropertiesmap-syntax.json"></a>

```
{
  "[OperatorPropertyKey](#cfn-customerprofiles-integration-taskpropertiesmap-operatorpropertykey)" : String,
  "[Property](#cfn-customerprofiles-integration-taskpropertiesmap-property)" : String
}
```

### YAML<a name="aws-properties-customerprofiles-integration-taskpropertiesmap-syntax.yaml"></a>

```
  [OperatorPropertyKey](#cfn-customerprofiles-integration-taskpropertiesmap-operatorpropertykey): String
  [Property](#cfn-customerprofiles-integration-taskpropertiesmap-property): String
```

## Properties<a name="aws-properties-customerprofiles-integration-taskpropertiesmap-properties"></a>

`OperatorPropertyKey`  <a name="cfn-customerprofiles-integration-taskpropertiesmap-operatorpropertykey"></a>
The task property key\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Property`  <a name="cfn-customerprofiles-integration-taskpropertiesmap-property"></a>
The task property value\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)