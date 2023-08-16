# AWS::QuickSight::Analysis LocalNavigationConfiguration<a name="aws-properties-quicksight-analysis-localnavigationconfiguration"></a>

The navigation configuration for `CustomActionNavigationOperation`\.

## Syntax<a name="aws-properties-quicksight-analysis-localnavigationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-analysis-localnavigationconfiguration-syntax.json"></a>

```
{
  "[TargetSheetId](#cfn-quicksight-analysis-localnavigationconfiguration-targetsheetid)" : String
}
```

### YAML<a name="aws-properties-quicksight-analysis-localnavigationconfiguration-syntax.yaml"></a>

```
  [TargetSheetId](#cfn-quicksight-analysis-localnavigationconfiguration-targetsheetid): String
```

## Properties<a name="aws-properties-quicksight-analysis-localnavigationconfiguration-properties"></a>

`TargetSheetId`  <a name="cfn-quicksight-analysis-localnavigationconfiguration-targetsheetid"></a>
The sheet that is targeted for navigation in the same analysis\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `[\w\-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)