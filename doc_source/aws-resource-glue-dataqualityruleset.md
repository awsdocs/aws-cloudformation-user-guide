# AWS::Glue::DataQualityRuleset<a name="aws-resource-glue-dataqualityruleset"></a>

The `AWS::Glue::DataQualityRuleset` resource specifies a data quality ruleset with DQDL rules applied to a specified AWS Glue table\. For more information, see AWS Glue Data Quality in the AWS Glue Developer Guide\.

## Syntax<a name="aws-resource-glue-dataqualityruleset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-dataqualityruleset-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::DataQualityRuleset",
  "Properties" : {
      "[ClientToken](#cfn-glue-dataqualityruleset-clienttoken)" : Json,
      "[Description](#cfn-glue-dataqualityruleset-description)" : String,
      "[Name](#cfn-glue-dataqualityruleset-name)" : String,
      "[Ruleset](#cfn-glue-dataqualityruleset-ruleset)" : String,
      "[Tags](#cfn-glue-dataqualityruleset-tags)" : Json,
      "[TargetTable](#cfn-glue-dataqualityruleset-targettable)" : TargetTable
    }
}
```

### YAML<a name="aws-resource-glue-dataqualityruleset-syntax.yaml"></a>

```
Type: AWS::Glue::DataQualityRuleset
Properties: 
  [ClientToken](#cfn-glue-dataqualityruleset-clienttoken): Json
  [Description](#cfn-glue-dataqualityruleset-description): String
  [Name](#cfn-glue-dataqualityruleset-name): String
  [Ruleset](#cfn-glue-dataqualityruleset-ruleset): String
  [Tags](#cfn-glue-dataqualityruleset-tags): Json
  [TargetTable](#cfn-glue-dataqualityruleset-targettable): 
    TargetTable
```

## Properties<a name="aws-resource-glue-dataqualityruleset-properties"></a>

`ClientToken`  <a name="cfn-glue-dataqualityruleset-clienttoken"></a>
Used for idempotency and is recommended to be set to a random ID \(such as a UUID\) to avoid creating or starting multiple instances of the same resource\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-glue-dataqualityruleset-description"></a>
A description of the data quality ruleset\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-dataqualityruleset-name"></a>
The name of the data quality ruleset\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Ruleset`  <a name="cfn-glue-dataqualityruleset-ruleset"></a>
A Data Quality Definition Language \(DQDL\) ruleset\. For more information see the AWS Glue Developer Guide\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-glue-dataqualityruleset-tags"></a>
A list of tags applied to the data quality ruleset\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetTable`  <a name="cfn-glue-dataqualityruleset-targettable"></a>
An object representing an AWS Glue table\.  
*Required*: Yes  
*Type*: [TargetTable](aws-properties-glue-dataqualityruleset-targettable.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-glue-dataqualityruleset-return-values"></a>

### Ref<a name="aws-resource-glue-dataqualityruleset-return-values-ref"></a>