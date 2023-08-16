# AWS::QuickSight::Template LocalNavigationConfiguration<a name="aws-properties-quicksight-template-localnavigationconfiguration"></a>

The navigation configuration for `CustomActionNavigationOperation`\.

## Syntax<a name="aws-properties-quicksight-template-localnavigationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-template-localnavigationconfiguration-syntax.json"></a>

```
{
  "[TargetSheetId](#cfn-quicksight-template-localnavigationconfiguration-targetsheetid)" : String
}
```

### YAML<a name="aws-properties-quicksight-template-localnavigationconfiguration-syntax.yaml"></a>

```
  [TargetSheetId](#cfn-quicksight-template-localnavigationconfiguration-targetsheetid): String
```

## Properties<a name="aws-properties-quicksight-template-localnavigationconfiguration-properties"></a>

`TargetSheetId`  <a name="cfn-quicksight-template-localnavigationconfiguration-targetsheetid"></a>
The sheet that is targeted for navigation in the same analysis\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)