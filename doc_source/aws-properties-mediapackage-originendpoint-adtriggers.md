# AWS::MediaPackage::OriginEndpoint AdTriggers<a name="aws-properties-mediapackage-originendpoint-adtriggers"></a>

The SCTE\-35 message types that MediaPackage treats as ad markers in the output manifest\. For information about SCTE\-35 in MediaPackage, see [SCTE\-35 Message Options in AWS Elemental MediaPackage](https://docs.aws.amazon.com/mediapackage/latest/ug/scte.html)\. 

## Syntax<a name="aws-properties-mediapackage-originendpoint-adtriggers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-mediapackage-originendpoint-adtriggers-syntax.json"></a>

```
{
  "[AdTriggers](#cfn-mediapackage-originendpoint-adtriggers-adtriggers)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-mediapackage-originendpoint-adtriggers-syntax.yaml"></a>

```
  [AdTriggers](#cfn-mediapackage-originendpoint-adtriggers-adtriggers): 
    - String
```

## Properties<a name="aws-properties-mediapackage-originendpoint-adtriggers-properties"></a>

`AdTriggers`  <a name="cfn-mediapackage-originendpoint-adtriggers-adtriggers"></a>
The SCTE\-35 message types that MediaPackage treats as ad markers in the output manifest\. For information about SCTE\-35 in MediaPackage, see [SCTE\-35 Message Options in AWS Elemental MediaPackage](https://docs.aws.amazon.com/mediapackage/latest/ug/scte.html)\.   
*Required*: No  
*Type*: [List](#aws-properties-mediapackage-originendpoint-adtriggers) of [String](#aws-properties-mediapackage-originendpoint-adtriggers)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)