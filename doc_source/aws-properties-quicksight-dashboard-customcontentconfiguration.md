# AWS::QuickSight::Dashboard CustomContentConfiguration<a name="aws-properties-quicksight-dashboard-customcontentconfiguration"></a>

The configuration of a `CustomContentVisual`\.

## Syntax<a name="aws-properties-quicksight-dashboard-customcontentconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-dashboard-customcontentconfiguration-syntax.json"></a>

```
{
  "[ContentType](#cfn-quicksight-dashboard-customcontentconfiguration-contenttype)" : String,
  "[ContentUrl](#cfn-quicksight-dashboard-customcontentconfiguration-contenturl)" : String,
  "[ImageScaling](#cfn-quicksight-dashboard-customcontentconfiguration-imagescaling)" : String
}
```

### YAML<a name="aws-properties-quicksight-dashboard-customcontentconfiguration-syntax.yaml"></a>

```
  [ContentType](#cfn-quicksight-dashboard-customcontentconfiguration-contenttype): String
  [ContentUrl](#cfn-quicksight-dashboard-customcontentconfiguration-contenturl): String
  [ImageScaling](#cfn-quicksight-dashboard-customcontentconfiguration-imagescaling): String
```

## Properties<a name="aws-properties-quicksight-dashboard-customcontentconfiguration-properties"></a>

`ContentType`  <a name="cfn-quicksight-dashboard-customcontentconfiguration-contenttype"></a>
The content type of the custom content visual\. You can use this to have the visual render as an image\.  
*Required*: No  
*Type*: String  
*Allowed values*: `IMAGE | OTHER_EMBEDDED_CONTENT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContentUrl`  <a name="cfn-quicksight-dashboard-customcontentconfiguration-contenturl"></a>
The input URL that links to the custom content that you want in the custom visual\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageScaling`  <a name="cfn-quicksight-dashboard-customcontentconfiguration-imagescaling"></a>
The sizing options for the size of the custom content visual\. This structure is required when the `ContentType` of the visual is `'IMAGE'`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DO_NOT_SCALE | FIT_TO_HEIGHT | FIT_TO_WIDTH | SCALE_TO_VISUAL`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)