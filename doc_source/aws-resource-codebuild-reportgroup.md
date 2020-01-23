# AWS::CodeBuild::ReportGroup<a name="aws-resource-codebuild-reportgroup"></a>

 Creates a report group\. A report group contains a collection of reports\. 

## Syntax<a name="aws-resource-codebuild-reportgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codebuild-reportgroup-syntax.json"></a>

```
{
  "Type" : "AWS::CodeBuild::ReportGroup",
  "Properties" : {
      "[ExportConfig](#cfn-codebuild-reportgroup-exportconfig)" : [ReportExportConfig](aws-properties-codebuild-reportgroup-reportexportconfig.md),
      "[Name](#cfn-codebuild-reportgroup-name)" : String,
      "[Type](#cfn-codebuild-reportgroup-type)" : String
    }
}
```

### YAML<a name="aws-resource-codebuild-reportgroup-syntax.yaml"></a>

```
Type: AWS::CodeBuild::ReportGroup
Properties: 
  [ExportConfig](#cfn-codebuild-reportgroup-exportconfig): 
    [ReportExportConfig](aws-properties-codebuild-reportgroup-reportexportconfig.md)
  [Name](#cfn-codebuild-reportgroup-name): String
  [Type](#cfn-codebuild-reportgroup-type): String
```

## Properties<a name="aws-resource-codebuild-reportgroup-properties"></a>

`ExportConfig`  <a name="cfn-codebuild-reportgroup-exportconfig"></a>
 Information about the destination where the raw data of this `ReportGroup` is exported\.   
*Required*: Yes  
*Type*: [ReportExportConfig](aws-properties-codebuild-reportgroup-reportexportconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-codebuild-reportgroup-name"></a>
 The name of a `ReportGroup`\.   
*Required*: No  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `128`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-codebuild-reportgroup-type"></a>
 The type of the `ReportGroup`\. The one valid value is `TEST`\.   
*Required*: Yes  
*Type*: String  
*Allowed Values*: `TEST`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)