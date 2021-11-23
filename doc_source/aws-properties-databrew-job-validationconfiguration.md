# AWS::DataBrew::Job ValidationConfiguration<a name="aws-properties-databrew-job-validationconfiguration"></a>

Configuration for data quality validation\. Used to select the Rulesets and Validation Mode to be used in the profile job\. When ValidationConfiguration is null, the profile job will run without data quality validation\.

## Syntax<a name="aws-properties-databrew-job-validationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-job-validationconfiguration-syntax.json"></a>

```
{
  "[RulesetArn](#cfn-databrew-job-validationconfiguration-rulesetarn)" : String,
  "[ValidationMode](#cfn-databrew-job-validationconfiguration-validationmode)" : String
}
```

### YAML<a name="aws-properties-databrew-job-validationconfiguration-syntax.yaml"></a>

```
  [RulesetArn](#cfn-databrew-job-validationconfiguration-rulesetarn): String
  [ValidationMode](#cfn-databrew-job-validationconfiguration-validationmode): String
```

## Properties<a name="aws-properties-databrew-job-validationconfiguration-properties"></a>

`RulesetArn`  <a name="cfn-databrew-job-validationconfiguration-rulesetarn"></a>
The Amazon Resource Name \(ARN\) for the ruleset to be validated in the profile job\. The TargetArn of the selected ruleset should be the same as the Amazon Resource Name \(ARN\) of the dataset that is associated with the profile job\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValidationMode`  <a name="cfn-databrew-job-validationconfiguration-validationmode"></a>
Mode of data quality validation\. Default mode is “CHECK\_ALL” which verifies all rules defined in the selected ruleset\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)