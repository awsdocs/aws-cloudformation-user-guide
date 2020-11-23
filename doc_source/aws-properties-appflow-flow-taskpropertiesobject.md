# AWS::AppFlow::Flow TaskPropertiesObject<a name="aws-properties-appflow-flow-taskpropertiesobject"></a>

 A map used to store task\-related information\. The execution service looks for particular information based on the `TaskType`\. 

## Syntax<a name="aws-properties-appflow-flow-taskpropertiesobject-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appflow-flow-taskpropertiesobject-syntax.json"></a>

```
{
  "[Key](#cfn-appflow-flow-taskpropertiesobject-key)" : String,
  "[Value](#cfn-appflow-flow-taskpropertiesobject-value)" : String
}
```

### YAML<a name="aws-properties-appflow-flow-taskpropertiesobject-syntax.yaml"></a>

```
  [Key](#cfn-appflow-flow-taskpropertiesobject-key): String
  [Value](#cfn-appflow-flow-taskpropertiesobject-value): String
```

## Properties<a name="aws-properties-appflow-flow-taskpropertiesobject-properties"></a>

`Key`  <a name="cfn-appflow-flow-taskpropertiesobject-key"></a>
 The task property key\.   
*Allowed Values*: `VALUE | VALUES | DATA_TYPE | UPPER_BOUND | LOWER_BOUND | SOURCE_DATA_TYPE | DESTINATION_DATA_TYPE | VALIDATION_ACTION | MASK_VALUE | MASK_LENGTH | TRUNCATE_LENGTH | MATH_OPERATION_FIELDS_ORDER | CONCAT_FORMAT | SUBFIELD_CATEGORY_MAP`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-appflow-flow-taskpropertiesobject-value"></a>
 The task property value\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)