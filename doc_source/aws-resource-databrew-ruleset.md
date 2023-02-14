# AWS::DataBrew::Ruleset<a name="aws-resource-databrew-ruleset"></a>

Specifies a new ruleset that can be used in a profile job to validate the data quality of a dataset\.

## Syntax<a name="aws-resource-databrew-ruleset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-databrew-ruleset-syntax.json"></a>

```
{
  "Type" : "AWS::DataBrew::Ruleset",
  "Properties" : {
      "[Description](#cfn-databrew-ruleset-description)" : String,
      "[Name](#cfn-databrew-ruleset-name)" : String,
      "[Rules](#cfn-databrew-ruleset-rules)" : [ Rule, ... ],
      "[Tags](#cfn-databrew-ruleset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TargetArn](#cfn-databrew-ruleset-targetarn)" : String
    }
}
```

### YAML<a name="aws-resource-databrew-ruleset-syntax.yaml"></a>

```
Type: AWS::DataBrew::Ruleset
Properties: 
  [Description](#cfn-databrew-ruleset-description): String
  [Name](#cfn-databrew-ruleset-name): String
  [Rules](#cfn-databrew-ruleset-rules): 
    - Rule
  [Tags](#cfn-databrew-ruleset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TargetArn](#cfn-databrew-ruleset-targetarn): String
```

## Properties<a name="aws-resource-databrew-ruleset-properties"></a>

`Description`  <a name="cfn-databrew-ruleset-description"></a>
The description of the ruleset\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-databrew-ruleset-name"></a>
The name of the ruleset\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Rules`  <a name="cfn-databrew-ruleset-rules"></a>
Contains metadata about the ruleset\.  
*Required*: Yes  
*Type*: List of [Rule](aws-properties-databrew-ruleset-rule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-databrew-ruleset-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetArn`  <a name="cfn-databrew-ruleset-targetarn"></a>
The Amazon Resource Name \(ARN\) of a resource \(dataset\) that the ruleset is associated with\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-databrew-ruleset-return-values"></a>

### Ref<a name="aws-resource-databrew-ruleset-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, Ref returns the resource name\. For example, `{ "Ref": "myRuleset" }`\.

For an AWS Glue DataBrew ruleset named `myRuleset`, `Ref` returns the name of the ruleset\.