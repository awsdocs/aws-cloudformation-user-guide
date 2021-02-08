# AWS::Config::ConformancePack<a name="aws-resource-config-conformancepack"></a>

A conformance pack is a collection of AWS Config rules and remediation actions that can be easily deployed in an account and a region\. ConformancePack creates a service linked role in your account\. The service linked role is created only when the role does not exist in your account\. 

## Syntax<a name="aws-resource-config-conformancepack-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-config-conformancepack-syntax.json"></a>

```
{
  "Type" : "AWS::Config::ConformancePack",
  "Properties" : {
      "[ConformancePackInputParameters](#cfn-config-conformancepack-conformancepackinputparameters)" : [ ConformancePackInputParameter, ... ],
      "[ConformancePackName](#cfn-config-conformancepack-conformancepackname)" : String,
      "[DeliveryS3Bucket](#cfn-config-conformancepack-deliverys3bucket)" : String,
      "[DeliveryS3KeyPrefix](#cfn-config-conformancepack-deliverys3keyprefix)" : String,
      "[TemplateBody](#cfn-config-conformancepack-templatebody)" : String,
      "[TemplateS3Uri](#cfn-config-conformancepack-templates3uri)" : String
    }
}
```

### YAML<a name="aws-resource-config-conformancepack-syntax.yaml"></a>

```
Type: AWS::Config::ConformancePack
Properties: 
  [ConformancePackInputParameters](#cfn-config-conformancepack-conformancepackinputparameters): 
    - ConformancePackInputParameter
  [ConformancePackName](#cfn-config-conformancepack-conformancepackname): String
  [DeliveryS3Bucket](#cfn-config-conformancepack-deliverys3bucket): String
  [DeliveryS3KeyPrefix](#cfn-config-conformancepack-deliverys3keyprefix): String
  [TemplateBody](#cfn-config-conformancepack-templatebody): String
  [TemplateS3Uri](#cfn-config-conformancepack-templates3uri): String
```

## Properties<a name="aws-resource-config-conformancepack-properties"></a>

`ConformancePackInputParameters`  <a name="cfn-config-conformancepack-conformancepackinputparameters"></a>
A list of ConformancePackInputParameter objects\.  
*Required*: No  
*Type*: List of [ConformancePackInputParameter](aws-properties-config-conformancepack-conformancepackinputparameter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConformancePackName`  <a name="cfn-config-conformancepack-conformancepackname"></a>
Name of the conformance pack you want to create\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DeliveryS3Bucket`  <a name="cfn-config-conformancepack-deliverys3bucket"></a>
AWS Config stores intermediate files while processing conformance pack template\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeliveryS3KeyPrefix`  <a name="cfn-config-conformancepack-deliverys3keyprefix"></a>
The prefix for the Amazon S3 bucket\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateBody`  <a name="cfn-config-conformancepack-templatebody"></a>
A string containing full conformance pack template body\. Structure containing the template body with a minimum length of 1 byte and a maximum length of 51,200 bytes\.  
You can only use a YAML template with one resource type, that is, config rule and a remediation action\. 
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateS3Uri`  <a name="cfn-config-conformancepack-templates3uri"></a>
Location of file containing the template body \(s3://bucketname/prefix\)\. The uri must point to the conformance pack template \(max size: 300 KB\) that is located in an Amazon S3 bucket\.  
You must have access to read Amazon S3 bucket\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-config-conformancepack-return-values"></a>

### Ref<a name="aws-resource-config-conformancepack-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the conformance pack\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-config-conformancepack--examples"></a>



### Conformance Pack<a name="aws-resource-config-conformancepack--examples--Conformance_Pack"></a>

The following example creates a conformance pack\.

#### JSON<a name="aws-resource-config-conformancepack--examples--Conformance_Pack--json"></a>

```
{
    "Resources": {
        "ConformancePack": {
            "Type": "AWS::Config::ConformancePack",
            "Properties": {
                "ConformancePackName": "ConformancePackName",
                "DeliveryS3Bucket": "DeliveryS3Bucket",
                "TemplateS3Uri": "s3://bucketname/prefix"            
            }
        }
    }
}
```

#### YAML<a name="aws-resource-config-conformancepack--examples--Conformance_Pack--yaml"></a>

```
---
AWSTemplateFormatVersion: 2010-09-09
Resources:
    CloudFormationCanaryPack:
        Type: AWS::Config::ConformancePack
        Properties:
          ConformancePackName: ConformancePackName
          DeliveryS3Bucket: DeliveryS3Bucket
          TemplateS3Uri: s3://bucketname/prefix
```