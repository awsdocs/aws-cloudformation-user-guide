# AWS::AccessAnalyzer::Analyzer<a name="aws-resource-accessanalyzer-analyzer"></a>

The `AWS::AccessAnalyzer::Analyzer` resource specifies a new analyzer\. The analyzer is an object that represents the IAM Access Analyzer feature\. An analyzer is required for Access Analyzer to become operational\.

## Syntax<a name="aws-resource-accessanalyzer-analyzer-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-accessanalyzer-analyzer-syntax.json"></a>

```
{
  "Type" : "AWS::AccessAnalyzer::Analyzer",
  "Properties" : {
      "[AnalyzerName](#cfn-accessanalyzer-analyzer-analyzername)" : String,
      "[ArchiveRules](#cfn-accessanalyzer-analyzer-archiverules)" : [ ArchiveRule, ... ],
      "[Tags](#cfn-accessanalyzer-analyzer-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-accessanalyzer-analyzer-type)" : String
    }
}
```

### YAML<a name="aws-resource-accessanalyzer-analyzer-syntax.yaml"></a>

```
Type: AWS::AccessAnalyzer::Analyzer
Properties: 
  [AnalyzerName](#cfn-accessanalyzer-analyzer-analyzername): String
  [ArchiveRules](#cfn-accessanalyzer-analyzer-archiverules): 
    - ArchiveRule
  [Tags](#cfn-accessanalyzer-analyzer-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-accessanalyzer-analyzer-type): String
```

## Properties<a name="aws-resource-accessanalyzer-analyzer-properties"></a>

`AnalyzerName`  <a name="cfn-accessanalyzer-analyzer-analyzername"></a>
The name of the analyzer\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ArchiveRules`  <a name="cfn-accessanalyzer-analyzer-archiverules"></a>
Specifies the archive rules to add for the analyzer\.  
*Required*: No  
*Type*: List of [ArchiveRule](aws-properties-accessanalyzer-analyzer-archiverule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-accessanalyzer-analyzer-tags"></a>
The tags to apply to the analyzer\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-accessanalyzer-analyzer-type"></a>
The type represents the zone of trust for the analyzer\.  
*Allowed Values*: ACCOUNT \| ORGANIZATION   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-accessanalyzer-analyzer-return-values"></a>

### Ref<a name="aws-resource-accessanalyzer-analyzer-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the analyzer created\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-accessanalyzer-analyzer--examples"></a>



### Declare an Analyzer Resource<a name="aws-resource-accessanalyzer-analyzer--examples--Declare_an_Analyzer_Resource"></a>

The following example shows how to declare a IAM Access Analyzer `Analyzer` resource:

#### JSON<a name="aws-resource-accessanalyzer-analyzer--examples--Declare_an_Analyzer_Resource--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "Analyzer": {
      "Properties": {
        "AnalyzerName": "DevAccountAnalyzer",
        "ArchiveRules": [
          {
            "Filter": [
              {
                "Eq": [
                  "123456789012"
                ],
                "Property": "principal.AWS"
              }
            ],
            "RuleName": "ArchiveTrustedAccountAccess"
          },
          {
            "Filter": [
              {
                "Contains": [
                  "arn:aws:s3:::docs-bucket",
                  "arn:aws:s3:::clients-bucket"
                ],
                "Property": "resource"
              }
            ],
            "RuleName": "ArchivePublicS3BucketsAccess"
          }
        ],
        "Tags": [
          {
            "Key": "Kind",
            "Value": "Dev"
          }
        ],
        "Type": "ACCOUNT"
      },
      "Type": "AWS::AccessAnalyzer::Analyzer"
    }
  }
}
```

#### YAML<a name="aws-resource-accessanalyzer-analyzer--examples--Declare_an_Analyzer_Resource--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  Analyzer:
    Type: 'AWS::AccessAnalyzer::Analyzer'
    Properties:
      AnalyzerName: MyAccountAnalyzer
      Type: ACCOUNT
      Tags:
        -
          Key: Kind
          Value: Dev
      ArchiveRules:
        -
          # Archive findings for a trusted AWS account
          RuleName: ArchiveTrustedAccountAccess
          Filter:
            -
              Property: 'principal.AWS'
              Eq:
                - '123456789012'
        -
          # Archive findings for known public S3 buckets
          RuleName: ArchivePublicS3BucketsAccess
          Filter:
            -
              Property: 'resource'
              Contains:
                - 'arn:aws:s3:::docs-bucket'
                - 'arn:aws:s3:::clients-bucket'
```