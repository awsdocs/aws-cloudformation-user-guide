# AWS::Macie::AllowList Criteria<a name="aws-properties-macie-allowlist-criteria"></a>

Specifies the criteria for an allow list, which is a list that defines specific text or a text pattern to ignore when inspecting data sources for sensitive data\. The criteria can be:
+ The location and name of an Amazon Simple Storage Service \(Amazon S3\) object that lists specific, predefined text to ignore \(`S3WordsList`\), or 
+ A regular expression \(`Regex`\) that defines a text pattern to ignore\.

The criteria must specify either an S3 object or a regular expression\. It can't specify both\.

## Syntax<a name="aws-properties-macie-allowlist-criteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-macie-allowlist-criteria-syntax.json"></a>

```
{
  "[Regex](#cfn-macie-allowlist-criteria-regex)" : String,
  "[S3WordsList](#cfn-macie-allowlist-criteria-s3wordslist)" : S3WordsList
}
```

### YAML<a name="aws-properties-macie-allowlist-criteria-syntax.yaml"></a>

```
  [Regex](#cfn-macie-allowlist-criteria-regex): String
  [S3WordsList](#cfn-macie-allowlist-criteria-s3wordslist): 
    S3WordsList
```

## Properties<a name="aws-properties-macie-allowlist-criteria-properties"></a>

`Regex`  <a name="cfn-macie-allowlist-criteria-regex"></a>
The regular expression \(*regex*\) that defines the text pattern to ignore\. The expression can contain 1\-512 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`S3WordsList`  <a name="cfn-macie-allowlist-criteria-s3wordslist"></a>
The location and name of an Amazon S3 object that lists specific text to ignore\.  
*Required*: No  
*Type*: [S3WordsList](aws-properties-macie-allowlist-s3wordslist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)