# AWS::CustomerProfiles::CalculatedAttributeDefinition AttributeDetails<a name="aws-properties-customerprofiles-calculatedattributedefinition-attributedetails"></a>

Mathematical expression and a list of attribute items specified in that expression\.

## Syntax<a name="aws-properties-customerprofiles-calculatedattributedefinition-attributedetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-customerprofiles-calculatedattributedefinition-attributedetails-syntax.json"></a>

```
{
  "[Attributes](#cfn-customerprofiles-calculatedattributedefinition-attributedetails-attributes)" : [ AttributeItem, ... ],
  "[Expression](#cfn-customerprofiles-calculatedattributedefinition-attributedetails-expression)" : String
}
```

### YAML<a name="aws-properties-customerprofiles-calculatedattributedefinition-attributedetails-syntax.yaml"></a>

```
  [Attributes](#cfn-customerprofiles-calculatedattributedefinition-attributedetails-attributes): 
    - AttributeItem
  [Expression](#cfn-customerprofiles-calculatedattributedefinition-attributedetails-expression): String
```

## Properties<a name="aws-properties-customerprofiles-calculatedattributedefinition-attributedetails-properties"></a>

`Attributes`  <a name="cfn-customerprofiles-calculatedattributedefinition-attributedetails-attributes"></a>
Mathematical expression and a list of attribute items specified in that expression\.  
*Required*: Yes  
*Type*: List of [AttributeItem](aws-properties-customerprofiles-calculatedattributedefinition-attributeitem.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Expression`  <a name="cfn-customerprofiles-calculatedattributedefinition-attributedetails-expression"></a>
Mathematical expression that is performed on attribute items provided in the attribute list\. Each element in the expression should follow the structure of \\"\{ObjectTypeName\.AttributeName\}\\"\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)