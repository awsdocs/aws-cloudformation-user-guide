# AWS::QuickSight::Dashboard FieldSort<a name="aws-properties-quicksight-dashboard-fieldsort"></a>

The sort configuration for a field in a field well\.

## Syntax<a name="aws-properties-quicksight-dashboard-fieldsort-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-fieldsort-syntax.json"></a>

```
{
  "[Direction](#cfn-quicksight-dashboard-fieldsort-direction)" : String,
  "[FieldId](#cfn-quicksight-dashboard-fieldsort-fieldid)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-fieldsort-syntax.yaml"></a>

```
  [Direction](#cfn-quicksight-dashboard-fieldsort-direction): String
  [FieldId](#cfn-quicksight-dashboard-fieldsort-fieldid): String
```

## Properties<a name="aws-properties-quicksight-dashboard-fieldsort-properties"></a>

`Direction`  <a name="cfn-quicksight-dashboard-fieldsort-direction"></a>
The sort direction\. Choose one of the following options:  
+  `ASC`: Ascending
+  `DESC`: Descending
*Required*: Yes  
*Type*: String  
*Allowed values*: `ASC | DESC`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldId`  <a name="cfn-quicksight-dashboard-fieldsort-fieldid"></a>
The sort configuration target field\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)