# AWS::QuickSight::Template FieldSort<a name="aws-properties-quicksight-template-fieldsort"></a>

The sort configuration for a field in a field well\.

## Syntax<a name="aws-properties-quicksight-template-fieldsort-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-fieldsort-syntax.json"></a>

```
{
  "[Direction](#cfn-quicksight-template-fieldsort-direction)" : String,
  "[FieldId](#cfn-quicksight-template-fieldsort-fieldid)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-fieldsort-syntax.yaml"></a>

```
  [Direction](#cfn-quicksight-template-fieldsort-direction): String
  [FieldId](#cfn-quicksight-template-fieldsort-fieldid): String
```

## Properties<a name="aws-properties-quicksight-template-fieldsort-properties"></a>

`Direction`  <a name="cfn-quicksight-template-fieldsort-direction"></a>
The sort direction\. Choose one of the following options:  
+  `ASC`: Ascending
+  `DESC`: Descending
*Required*: Yes  
*Type*: String  
*Allowed values*: `ASC | DESC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-template-fieldsort-fieldid"></a>
The sort configuration target field\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)